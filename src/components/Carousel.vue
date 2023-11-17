<script setup>
import { ref } from 'vue';


// Guardamos las props en una variable, para poder acceder a ellas
const props = defineProps(['images'])

// Variable de estado para determinar en que índice del array de imágenes me encuentro
const index = ref(0)

const left = () => {
    index.value--;
    if (index.value==-1) {index.value=props.images.length-1}
}

const right = () => {
    index.value++;
    if (index.value==props.images.length) {index.value=0}
}


</script>

<template>
  <div>
    <button v-on:click="left">Left</button>
    <img  v-bind:src=" images[index]" alt="" />
    <button @click="right">Right</button>
  </div>
</template>

<style scoped></style>
