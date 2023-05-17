<script setup>
   import MenuCom from '../components/MenuCom.vue'
   import CardCom from '../components/CardCom.vue';
   
   const cards = [
     {
       image: 'https://steamuserimages-a.akamaihd.net/ugc/945090495170688918/72AD2559E6AC9C317D9BB61CFF442F1719550808/?imw=512&&ima=fit&impolicy=Letterbox&imcolor=%23000000&letterbox=false',
       content: 'David Laid'
     },
     {
       image: 'https://steamuserimages-a.akamaihd.net/ugc/1686022974569379369/704F34CCA86A7C85977987DCBF075C40041C8FC4/?imw=512&&ima=fit&impolicy=Letterbox&imcolor=%23000000&letterbox=false',
       content: 'Chris Bumstead'
     },
     {
       image: 'https://i.playboard.app/p/4835ea60dcf2376015bfeda73db9541a/default.jpg',
       content: 'Daddy Aioli'
     },
     {
       image: 'https://laletrade.com/images/jamp/page/Carlos-Belcast.jpg',
       content: 'Carlos Belcast'
     },
     
   ];
</script>
   
<template>
    <MenuCom></MenuCom>
    <main class="row text-center d-flex justify-content-center gap-3 p-3">
       <h2>Entrenadores</h2>
       <CardCom v-for="(card, index) in cards" :key="index" :image="card.image" :content="card.content"></CardCom>
    </main>
</template>
   
<style scoped>
   h2 {
     margin-top: 60px;
   }
</style>