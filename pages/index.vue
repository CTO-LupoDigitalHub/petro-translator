<template>
<div>
<petro-logo></petro-logo>
<index-search></index-search>
</div>
</template>

<script>
import PetroLogo from '../components/PetroLogo'
import IndexSearch from '../components/IndexSearch'
export default {
  components: { PetroLogo, IndexSearch },
  name: 'IndexPage'
}
</script>
