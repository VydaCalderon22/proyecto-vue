<script>
import {defineProps} from 'vue';

const props = defineProps(
    [
        'resultado'
    ]
);


</script>

<template>
    <!-- Resultado de la clase computada-->
    <div class="resultado">
        {{ props.resultado }}
    </div>
</template>

