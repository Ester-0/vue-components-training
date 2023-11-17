<script setup>
import { ref } from 'vue';


const likes = ref(0)

// podemos dejarlo así porque esta variable realmente no la usamos para mostrarla en el <template> ni para gestionar ningún formulario
let indexColor = 0

const colors = ['purple', 'blue', 'green', 'yellow', 'orange', 'red']


const incrementLikes = () => {
    likes.value++;

    // Reto: Cómo modificar la variable indexColor para que vaya iterando por el array de colores
    // Puede que evenutalmente os de un error, mirad la consola

    // Corregir: 10.17
    
    indexColor= indexColor+1
    if (indexColor==6) {indexColor=0}

}

</script>

<template>
    <!-- La directiva v-on sirve para gestionar los eventos. Lo que hace este código es que al hacer click en el botón, incrementamos la variable de estado 'likes'-->

    <!-- La directiva v-bind sirve para hacer cualquier atributo dinámico. El valor del atributo pasa a ser una expresión JavaScript-->
    <button v-bind:style="{ backgroundColor: colors[indexColor] }" v-on:click="incrementLikes">{{ likes }} Likes</button>
</template>

<style scoped></style>