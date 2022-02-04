<template>
  <div>
    <b-modal
      v-model="modalShow"
      header-class="justify-content-center"
      header-text-variant="primary"
      centered
      hide-footer
      size='lg'
      title="¡HASTA LA VISTA MENTIRAS!">
        <div class="text-center">
          Harvard estima que cada hora le inventan 1.5 noticias falsas a Petro.
          <br>Verifica con Terminator lo que <strong>SÍ propone</strong> y lo <strong>Sí dice Petro.</strong>
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
