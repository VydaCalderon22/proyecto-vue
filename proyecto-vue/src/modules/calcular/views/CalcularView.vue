<script setup>
    import { ref, computed } from 'vue'; 
    import ResultadoSection from '../components/ResultadoSection.vue';
    const valor = ref('');

    // Propiedad computada que duplica el valor ingresado
    const valorCalculado = computed(() => {
        return valor.value * 3;
    });

    const mostrarElemento = computed(() => {
        return valor.value;
    });

</script>


<template>
    
    <h3>Propiedades computadas </h3>
    <input type="text" v-model="valor"/>
    {{ valorCalculado }}

    <!-- Se agrega la directiva que se creo como propiedad, se envía su variable reactiva (valorCalculado) -->
    <ResultadoSection v-if="mostrarElemento" :resultado="valorCalculado"></ResultadoSection>
    <div v-else-if="isNaN(valor)"> </div>
    <div v-else> Aquí no se muestra nada, si el v-if no se cumple </div>
</template>