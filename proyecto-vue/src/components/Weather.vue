<script setup>
import { onMounted } from "vue";
import { useWeatherStore } from "../stores/weatherStore";
import { useWeather } from "../composables/useWeather"; 

const weatherStore = useWeatherStore();

onMounted(() => {
    useWeather();
});
</script>

<template>
<h3> La temperatura actual es: {{ weatherStore.temperatura }}°C</h3>
</template>
