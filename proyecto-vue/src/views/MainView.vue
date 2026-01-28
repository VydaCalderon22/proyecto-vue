<script setup>
import SideBar from '../components/SideBar.vue';
import Header from '../components/Header.vue';
import { ref } from 'vue';

const texto = ref('');
</script>


<template>
    <Header></Header>

    <div class="container">
        <SideBar></SideBar> 
        <div class="content">
            <input v-model="texto" placeholder="Escribe algo..." />
            {{ texto }}
            <router-view></router-view>
        </div>

    </div>
</template>

<style>
.container{
    display: flex;

}
.content{
   flex: 1;
   padding: 20px; 
}
</style>