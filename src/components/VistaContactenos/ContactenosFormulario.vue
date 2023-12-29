<template>
    <v-sheet
        height="auto"
        width="auto"
    >
    <form @submit.prevent="submit" >
    <v-row>
      <v-col>
        
      <v-text-field
        clearable
        v-model="name.value.value"
        :counter="30"
        :error-messages="name.errorMessage.value"
        label="Nombre"
        prepend-icon="mdi-account"
      ></v-text-field>
  
      <v-text-field
        clearable
        v-model="phone.value.value"
        :counter="30"
        :error-messages="phone.errorMessage.value"
        label="Numero de celular"
        prepend-icon="mdi-cellphone"
      ></v-text-field>
      </v-col>  
      <v-col>
      <v-text-field
        clearable
        v-model="email.value.value"
        :error-messages="email.errorMessage.value"
        label="Correo"
        prepend-icon="mdi-email"
      ></v-text-field>
      
      
      <v-text-field
        clearable
        v-model="asunto.value.value"
        :counter="10"
        :error-messages="asunto.errorMessage.value"
        label="Asunto"
        prepend-icon="mdi-card-account-mail"
      ></v-text-field>
    </v-col>
    </v-row>
    
      <v-textarea 
            class="prepend-icon"
            clearable

            v-model="mensaje.value.value"
            :counter="100"
            :error-messages="mensaje.errorMessage.value"

            label="Mensaje"
            prepend-icon="mdi-message"
            variant="solo-filled"
        ></v-textarea>  
    <v-divider :thickness="20" class="border-opacity-0"></v-divider>
    <v-row class="align-center justify-center">
      <v-btn
        style="background-color: #f4a414;"
        class="me-4"
        type="submit"
      >
        Enviar
      </v-btn>
  
      <v-btn @click="handleReset" style="background-color: #f4a414;">
        Limpiar
      </v-btn>
    </v-row>
      
    <!--
  
      <v-checkbox
        clearable
        v-model="checkbox.value.value"
        :error-messages="checkbox.errorMessage.value"
        value="1"
        label="Option"
        type="checkbox"
      ></v-checkbox>
    -->

    </form>
    </v-sheet>
  </template>

<script setup>
  import { ref } from 'vue'
  import { useField, useForm } from 'vee-validate'

  const { handleSubmit, handleReset } = useForm({
    validationSchema: {
      name (value) {
        if (value?.length >= 3) return true

        return 'El nombre requiere mas de dos caracteres'
      },
      phone (value) {
        if (value?.length > 9 && /[0-9-]+/.test(value)) return true

        return 'El numero de celular requiere mas de 8 digitos'
      },
      email (value) {
        if (/^[a-z.-]+@[a-z.-]+\.[a-z]+$/i.test(value)) return true

        return 'Email invalido'
      },
      asunto (value) {
        if (value?.length >= 7) return true

        return 'El asunto debe tener mas de 6 digitos'
      },
      checkbox (value) {
        if (value === '1') return true

        return 'Debe ser revisado.'
      },
      mensaje (value) {
        if (value?.length >= 10) return true

        return 'El asunto debe tener mas de 9 digitos'
      },
    },
  })
  const name = useField('name')
  const phone = useField('phone')
  const email = useField('email')
  const asunto = useField('asunto')
  const mensaje = useField('mensaje')
  const checkbox = useField('checkbox')



  const submit = handleSubmit(values => {
    alert(JSON.stringify(values, null, 2))
  })
</script>  
<style>
  .prepend-icon{
    color: rgb(0, 0, 0);
  }
</style>