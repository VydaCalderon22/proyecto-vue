<script setup>

</script>

<template>
    <div class="sidebar">
        <h2>Barra lateral</h2>
        <ul>
            <!-- Enlaces para los componentes -->
            <li><router-link to="/contador">Contador</router-link></li>
            <li><router-link to="/lista-de-tareas">Lista de tareas</router-link></li>
            <li><router-link to="/registro">Registrar</router-link></li>
        </ul>
    </div>
</template>

<style>
.sidebar{
    width: 200px;
    background-color: #d0eaff;
    padding: 15px;
}

</style>