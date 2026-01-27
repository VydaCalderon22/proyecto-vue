<script setup>
import { ref } from 'vue';
const contador = ref(0);

// Función flecha para incrementar el contador
const incrementar = () => {
  // El value permite cambiar el valor de una varible reactiva
  contador.value++;
};


// Función flecha para decrementar el contador  
const decrementar = () => {
  contador.value--;
};


</script>

<template>
  <h1>Hello Vue!</h1>
  <p> {{ contador }} </p>

  <!--Llama a la función incrementar al hacer click -->
  <button @click="incrementar">Incrementar</button>

  <!--Llama a la función decrementar al hacer click -->
  <button @click="decrementar">Decrementar</button>
</template>

<style scoped>

p{
  color: blue;
}
</style>
