<template>
  <div>
    <b-modal
      v-model="modalShow"
      header-class="justify-content-center"
      header-text-variant="primary"
      centered
      hide-footer
      size='lg'
      title="DALE TRANSLATOR A LAS MENTIRAS">
        <div class="text-center">
        Con el <strong>Petro-translator</strong> infórmate sobre lo que significa para Petro acuerdo de paz, exportación, democracia y muchas palabras más.
        </div>
    </b-modal>
  </div>
</template>
<script>
export default {
  name: 'MessageModal',
  data() {
      return {
        modalShow: true
      }
    }
}
</script>
