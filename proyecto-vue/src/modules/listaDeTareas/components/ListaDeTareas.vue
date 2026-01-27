<script setup>
import { ref } from 'vue';

const tareas = ref([]);

const nuevaTarea = ref('');

const addTarea = () => {
    if (nuevaTarea.value !== '') {
        tareas.value.push(nuevaTarea.value);
        nuevaTarea.value = '';
    }
}

// Función para borrar una tarea por su índice, ese valor se asigno en la directiva v-for
const borrarTarea = (index) => {
    tareas.value.splice(index, 1);
}

</script>

<template>
    <div>
        <h2>Lista de tareas</h2>
        <input type="text" v-model="nuevaTarea" @keyup.enter="addTarea" placeholder="Escribe una tarea y presiona enter"/>
        <ul>
            <li v-for="(tarea, index) in tareas" :key="index">
                {{ tarea }}
                <button @click="borrarTarea(index)">Borrar esta tarea</button>
            </li>
        </ul>     
    </div>
</template>



<style scoped>
</style>
