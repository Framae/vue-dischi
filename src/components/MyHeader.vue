<template>
  <div class="sfondo">
    <img :src="image" alt="">
  </div>
   
</template>

<script>
export default {
    name: 'MyHeader',
    props: {
      image: String
    }
}
</script>

<style lang='scss' scoped>
  .sfondo {
    background-color: blue;
  }
  img {
    width: 30px;
    height: 30px;
  }
</style>