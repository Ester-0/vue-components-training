<script setup>
import IdCard from './components/IdCard.vue';
import Random from './components/Random.vue';



</script>



<template>
  <h1>Creación de componentes con Vue</h1>
  <section>
    <h2>Id Card</h2>
    <IdCard last-name='Doe' first-name='John' gender='male' :height="178" :birth='new Date("1992-07-14")'
      picture="https://randomuser.me/api/portraits/men/44.jpg" />
  
    
    <IdCard last-name='Dolores' first-name='Obrien' gender='female' :height="172" :birth='new Date("1993-05-11")'
      picture="https://randomuser.me/api/portraits/women/8.jpg" />
  </section>
  
<section>
  <h1>Random</h1>
  <Random :min="1" :max="6"/>
<Random :min="1" :max="100"/>

<!-- <Random min="1" max="6" :numRandom="Math.floor(Math.random() * 'max') + 1"/> -->


</section>

</template>





<style scoped>
h2 {
  color: blueviolet;
}
</style>
