<script setup>
import Weather from './Weather.vue';
</script>


<template>
    <div class="header">
        <Weather></Weather>
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