<template>
  <b-container class="bv-row">
    <b-card
      header-tag="header"
      no-body
      header-bg-variant="white"
      class="text-center"
    >
      <template #header>
        <h6 class="mb-0 py-2">
          TERMINA CON LOS RUMORES Y LAS MENTIRAS DE LOS ODIADORES.
        </h6>
      </template>

      <b-row class="sm-col">
        <b-col>
          <div v-if="search" @click="$emit('reset')" class="close" />
          <b-form-textarea
            :value="search"
            :debounce="350"
            @input="(value) => $emit('update:search', value)"
            class="txtEr8xn"
            id="textarea-auto-height"
            placeholder="Escribe la palabra o frase que quieras consultar y el TERMINATOR DE LA DESINFORMACIÓN te dirá la verdad."
            rows="5"
            max-rows="15"
          ></b-form-textarea>
        </b-col>
        <b-col class="border-text-area">
          <b-list-group>
            <b-list-group-item
              v-for="item in list"
              :key="item.id"
              class="border-0 text-left"
            >
              <p class="mb-0">
                <strong>{{ item.name }}</strong>
              </p>
              <p class="mb-0" style="font-size: 12px; line-height: 15px">
                {{ item.description }}
              </p>
            </b-list-group-item>
          </b-list-group>
        </b-col>
      </b-row>
    </b-card>
        <b-container mt-5>
      <b-img
      src="~/assets/image/footer-banner.png"
      fluid
      />
    </b-container>
  </b-container>

</template>

<script>
export default {
  name: "IndexSearch",
  props: ["search", "list"],
};
</script>
