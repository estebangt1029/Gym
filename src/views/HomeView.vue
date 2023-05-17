<script setup>
   import MenuCom from '../components/MenuCom.vue'
   import PlanesCom from '../components/PlanesCom.vue';
   
   const planes = [
     {
       image: 'https://res.cloudinary.com/daqs7crna/image/upload/v1684285419/principiante_glp71u.png',
       content: '1 Dia',
       precio: '4500'
     },
     {
       image: 'https://res.cloudinary.com/daqs7crna/image/upload/v1684285391/intermedio_oslz1b.png',
       content: '15 Dias',
       precio: '30000'
     },
     {
       image: 'https://res.cloudinary.com/daqs7crna/image/upload/v1684285356/avanzado_ta2ynl.png',
       content: '1 Mes',
       precio: '50000'
     },
     {
       image: 'https://res.cloudinary.com/daqs7crna/image/upload/v1684284942/profesional_ljyao9.png',
       content: '1 Año',
       precio: '480000'
     },
     
   ];
</script>
<template>
    <MenuCom></MenuCom>
    <main class="row text-center d-flex justify-content-center gap-3 p-3">  
      <h2>Planes</h2>
        <PlanesCom v-for="(plan, index) in planes" :key="index" :image="plan.image" :content="plan.content" :precio="plan.precio"></PlanesCom>
    </main>
</template>
<style scoped>
  h2{
    margin-top: 60px;
  }
</style>