<template>
<v-responsive>
    <h1 class="text-center"  style="color: #5c5c5c;">Contáctanos</h1>

    <div>   
    <v-row>
        
        <v-col>
            
            <ContatenosMediosDeComunicacion/>
        </v-col>
    
        
        <v-col>
            <ContactenosFormulario/>
        </v-col>
        
    </v-row>
    </div> 
    <v-divider :thickness="60" class="border-opacity-0"></v-divider>
</v-responsive>
</template>
  
<script setup>
    import ContactenosFormulario from '@/components/VistaContactenos/ContactenosFormulario.vue';
    import ContatenosMediosDeComunicacion from '@/components/VistaContactenos/ContatenosMediosDeComunicacion.vue';
</script>

<style>

</style>
