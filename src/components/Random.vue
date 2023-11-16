<script setup>
defineProps(['min', 'max'])

</script>

<template>
    <div>
        <p>Random value between: {{ min }} and {{ max }} => {{ Math.floor(Math.random() * max -min+1) + min }} </p>
        
    </div>
</template>

<style></style>