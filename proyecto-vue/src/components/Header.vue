<script setup>
import Weather from './Weather.vue';
// Permite definir las props que el componente puede recibir de un componente padre
import { defineProps, ref, watch} from 'vue';

const props = defineProps(['mensaje'])
const mensajeRecibido = ref(props.mensaje);

watch(() => props.mensaje, (newVal) => {
    mensajeRecibido.value = newVal;
}); 


</script>


<template>
    <div class="header">
        <!-- Componente hijo y el padre es Header -->
        {{ mensajeRecibido }} <Weather></Weather>
    </div>
</template>

<style scoped>
.header{
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #b1becc;
    color: white;
    padding: 10px 20px;
    top: 0;
    right: 0;
    color: white;
    left: 0;
    text-align: center;
}
h3{
    margin: 0;
}
</style>