<template>
  <div>
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

  img {
    width: 30px;
    height: 30px;
  }
</style>