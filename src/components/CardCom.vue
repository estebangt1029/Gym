<template>
    <div class="card col-11 col-sm-4 col-lg-3 p-2">
      <img :src="image" alt="">
      <p>{{ content }}</p>
      <button class="btn btn-dark">Mas</button>
    </div>
</template>
  
<script>
  export default {
    props: {
      image: {
        type: String,
        required: true
      },
      content: {
        type: String,
        required: true
      }
    }
  }
</script>