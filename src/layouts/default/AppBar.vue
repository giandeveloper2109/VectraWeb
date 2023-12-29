<template>
  <v-app-bar  flat app class=" text-center d-flex flex-column">
    <v-divider :thickness="20" class="border-opacity-0" vertical></v-divider>
    <div>
      <router-link to="/">
        <v-img  class="mr-3" src="@/assets/vectra.png" height="100px" width="100px"></v-img>
      </router-link>

    </div>
    <v-spacer></v-spacer>
    <div>
      <v-btn to="/"  style="color: rgb(10, 10, 50);">Home</v-btn>
    </div>
    <v-divider  :thickness="7" class="border-opacity-0" vertical></v-divider>
    <div>
      <v-btn to="/contactanos" text style="color: rgb(10, 10, 50);">Contáctanos</v-btn>
    </div>
    <v-divider :thickness="7" class="border-opacity-0" vertical></v-divider>
    <!--
    <div>
      <v-btn text style="color: rgb(10, 10, 50);">Proyectos</v-btn>
    </div>
    <v-divider :thickness="7" class="border-opacity-0" vertical></v-divider>
    <div>
      <v-btn text style="color: rgb(10, 10, 50);">Nosotros</v-btn>
    </div>
    <v-divider :thickness="7" class="border-opacity-0" vertical></v-divider>
    <div>
      <v-btn text style="color: rgb(10, 10, 50);">Cotiza</v-btn>
    </div>
    -->
    <v-divider :thickness="7" class="border-opacity-0" vertical></v-divider>
    <div>
      <v-img @click="redirectToWhatsApp" src="@/assets/whatsapp.png" width="40px" ></v-img>
    </div>
    <v-divider :thickness="20" class="border-opacity-0" vertical></v-divider>
    <div>
      <v-img @click="redirectFacebook" src="@/assets/facebook.png" width="40px" ></v-img>
    </div>
    <v-divider :thickness="20" class="border-opacity-0" vertical></v-divider>
    <div >
      <v-img @click="redirectMail" src="@/assets/correo.png" width="40px" ></v-img>
    </div>
    <v-divider :thickness="20" class="border-opacity-0" vertical></v-divider>
    <div>
      <v-img  @click="redirectPhone" src="@/assets/telefono.png" width="30px" ></v-img>
    </div>
    <v-divider :thickness="20" class="border-opacity-0" vertical></v-divider>
  </v-app-bar>
</template>

<script setup>
const redirectToWhatsApp = () => {
  const phoneNumber = '51982010512';

// Abre la ventana de WhatsApp con el número de teléfono.
window.location.href = `https://wa.me/${phoneNumber}`;
};
const redirectFacebook = () => {
window.location.href = `https://www.facebook.com/muranoinm`;
};
const redirectMail = () =>{
  window.location.href = `mailto:info@muranoin.com`;
};
const redirectPhone = () =>{
  window.location.href = `tel:074600993`;
};

</script>
