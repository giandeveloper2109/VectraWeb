<template>
  <v-row>
    <v-col>
      <v-container class="fill-height">
    <v-responsive class="align-center text-center fill-height">
      <v-img height="250" src="@/assets/construccion.png" />

      <div class="text-h4 font-weight-light mb-n1">Bienvenidos a Vectra</div>

      <h1 class="text-h3 font-weight-bold">Estamos en construcción...</h1>

      <div class="py-14" />

    </v-responsive>
      </v-container>
    </v-col>

    <v-col>
      <v-container >
    <v-responsive class="align-center text-center fill-height">
      <ContatenosMediosDeComunicacion/>
    </v-responsive>
  </v-container>
    </v-col>
  </v-row>

</template>

<script setup>
  import ContatenosMediosDeComunicacion from './VistaContactenos/ContatenosMediosDeComunicacion.vue';
</script>
