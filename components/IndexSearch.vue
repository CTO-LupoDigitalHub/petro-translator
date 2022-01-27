<!-- Please remove this file from your project -->
<template>
  <b-container class="bv-row">
    <b-card header-tag="header" header-bg-variant="white" class="text-center">
      <template #header>
        <h6 class="mb-0 py-2">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis
          consectetur suscipit
        </h6>
      </template>
      <b-card-text>
        <b-row>
          <b-col>
            <b-form-textarea
              class="er8xn"
              id="textarea-auto-height"
              placeholder="Escriba su busqueda aquí..."
              rows="3"
              max-rows="8"
            ></b-form-textarea>
          </b-col>
          <b-col class="border-text-area">
            <b-list-group>
              <b-list-group-item class="border-0 text-left">Cras justo odio</b-list-group-item>
              <b-list-group-item class="border-0 text-left">Dapibus ac facilisis in</b-list-group-item>
              <b-list-group-item class="border-0 text-left">Morbi leo risus</b-list-group-item>
              <b-list-group-item class="border-0 text-left">Porta ac consectetur ac</b-list-group-item>
              <b-list-group-item class="border-0 text-left">Vestibulum at eros</b-list-group-item>
            </b-list-group>
          </b-col>
        </b-row>
      </b-card-text>
    </b-card>
  </b-container>
</template>

<script>
export default {
  name: "IndexSearch",
};
</script>
