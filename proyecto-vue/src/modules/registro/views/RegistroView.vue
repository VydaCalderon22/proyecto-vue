<script setup>
import { Form, Field, ErrorMessage } from 'vee-validate'; 
import { schema } from '../schemas/validationSchema.js';
import {useRegistrarStore} from '../stores/registrarStore.js';

import { ref } from 'vue';

const registrarStore = useRegistrarStore();

// Datos del formulario
const nombre = ref('');
const email = ref('');

// Función para manejar el envío del formulario
const onSubmit = () => {
    registrarStore.guardarRegistro(nombre.value, email.value);
    console.log('Se ha enviado el formulario');
};
</script>

<template>
    <div>
        <h2>Registro</h2>

        <Form :validation-schema="schema" @submit="onSubmit">
            <div class="form">
                <label for="nombre">Nombre:</label>
                <Field v-model="nombre" type="text" name="nombre" id="nombre" placeholder="Nombre"/>
                <ErrorMessage name="nombre" />
            </div>

            <div class="form">
                <label for="email">Correo electrónico:</label>
                <Field v-model="email" type="email" name="email" id="email" placeholder="Correo electrónico"/>
                <ErrorMessage name="email" />
            </div>
            <button type="submit">Registrar</button>
        </Form>
    </div>
</template>

<style scoped>
.form{
    margin-bottom: 15px;
}
</style>