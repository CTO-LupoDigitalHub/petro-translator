<template>
  <div>
    <petro-logo></petro-logo>
    <message-modal></message-modal>
    <index-search
      :search.sync='search'
      :list='list'
      @reset='reset'
    ></index-search>
  </div>
</template>

<script>
import PetroLogo from '../components/PetroLogo';
import IndexSearch from '../components/IndexSearch';
import MessageModal from '../components/MessageModal';
// import elasticlunr from 'elasticlunr';
import data from "assets/data/data";

var elasticlunr = require('elasticlunr');
require('@/assets/js/lunr.stemmer.support.js')(elasticlunr);
require('@/assets/js/lunr.es.js')(elasticlunr);

export default {
  components: {
    PetroLogo,
    IndexSearch,
    MessageModal
  },
  name: "IndexPage",
  data() {
    return {
      original: [],
      list: [],
      search: "",
      resuls: [],
      searchIndex: null,
    };
  },
  computed: {
    dataImport() {
      return data;
    },
  },
  watch: {
    search() {
      this.results = this.searchIndex.search(this.search);
      this.list = [];
      this.results.forEach((d) => {
        this.original.forEach((p) => {
          if (d.ref === p.name) {
            this.list.push(p);
          }
        });
      });
      if (this.search.length === 0) {
        this.reset();
      }
    },
  },
  mounted() {
    this.original = this.dataImport;
    this.buildIndex();
  },
  methods: {
    reset() {
      this.list = [];
      this.search = "";
    },
    buildIndex() {
      const documents = this.original;

      this.searchIndex = elasticlunr(function () {
        this.setRef("name");
        this.use(elasticlunr.es);
        this.addField("name");
        this.addField("description");

        documents.forEach((doc) => {
          this.addDoc(doc);
        });
      });
    }
  },
};
</script>
