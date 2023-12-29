<template>


        <v-sheet>
            
            <v-img src="@/assets/vectra.png" max-height="200"></v-img>


            <v-row>
                <v-col class="d-flex align-center justify-center">
                    <v-card  @click="redirectToPhone"
                        height="70"
                        width="250"
                        style="background-color: #000744;color: rgb(255, 255, 255);;"
                        class="d-flex align-center justify-center"

                    >
                        <v-row>
                            <v-col>
                                <v-divider :thickness="20" class="border-opacity-0" vertical></v-divider>
                                <v-icon class="icon-size" icon="mdi-phone"></v-icon>
                                <v-divider :thickness="10" class="border-opacity-0" vertical></v-divider>
                                <span>(074) 600 993</span>
                            </v-col>

                        </v-row>
                    </v-card>

                </v-col>


                <v-col class="d-flex align-center justify-center">
                    <v-card  @click="redirectToPhone"
                        height="70"
                        width="250"
                        style="background-color: #000744;color: rgb(255, 255, 255);;"
                        class="d-flex align-center justify-center"

                    >
                        <v-row>
                            <v-col>
                                <v-divider :thickness="20" class="border-opacity-0" vertical></v-divider>
                                <v-icon class="icon-size" style="color: rgb(38, 141, 28);" icon="mdi mdi-whatsapp"></v-icon>
                                <v-divider :thickness="10" class="border-opacity-0" vertical></v-divider>
                                <span>+51 982 010 512</span>
                            </v-col>

                        </v-row>
                    </v-card>

                </v-col>


                <v-col class="d-flex align-center justify-center">
                    <v-card
                        height="70"
                        width="250"
                        style="background-color: #000744;color: rgb(255, 255, 255);;"
                        class="d-flex align-center justify-center"

                    >
                        <v-row>
                            <v-col>
                                <v-divider :thickness="20" class="border-opacity-0" vertical></v-divider>
                                <v-icon icon="mdi mdi-map-marker"></v-icon>
                                <v-divider :thickness="10" class="border-opacity-0" vertical></v-divider>
                                <span>Calle 7 de Enero #660 Chiclayo</span>
                            </v-col>

                        </v-row>
                    </v-card>

                </v-col>


                <v-col class="d-flex align-center justify-center">
                    <v-card  @click="redirectMail"
                        height="70"
                        width="250"
                        style="background-color: #000744;color: rgb(255, 255, 255);;"
                        class="d-flex align-center justify-center"

                    >
                        <v-row>
                            <v-col>
                                <v-divider :thickness="20" class="border-opacity-0" vertical></v-divider>
                                <v-icon icon="mdi mdi-email"></v-icon>
                                <v-divider :thickness="10" class="border-opacity-0" vertical></v-divider>
                                <span>info@muranoin.com</span>
                            </v-col>

                        </v-row>
                    </v-card>

                </v-col>


                <v-col class="d-flex align-center justify-center">
                    <v-card
                        height="250"
                        width="600"


                    >
                        <v-row>
                            <v-col>
                                <div>
                                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d4711.614133749156!2d-79.83959854866583!3d-6.772356904702242!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x904cef29c74ae85b%3A0xa7d0b9f7daf53c55!2s7%20de%20Enero%20660%2C%20Chiclayo%2014001!5e0!3m2!1ses-419!2spe!4v1703630584893!5m2!1ses-419!2spe" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                                </div>
                            </v-col>

                        </v-row>
                    </v-card>

                </v-col>


            </v-row>



        </v-sheet>
        <v-divider :thickness="20" class="border-opacity-0"></v-divider>

</template>
<script>
export default {
  methods: {
    redirectToWhatsApp() {
      // Reemplaza '123456789' con el número de teléfono al que deseas redirigir en formato internacional.
      const phoneNumber = '51982010512';

      // Abre la ventana de WhatsApp con el número de teléfono.
      window.location.href = `https://wa.me/${phoneNumber}`;
    },
    redirectToPhone() {
        window.location.href = `tel:074600993`;
    },
    redirectMail () {
  window.location.href = `mailto:info@muranoin.com`;
}

  }
}
</script>
<style>
  .icon-size {
    font-size: 40px;
  }
</style>
