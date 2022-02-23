<template>
  <div id="app">
    <MyHeader :image="url"/>
    <MyMain   />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'
export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain
  },
  data() {
    return {
      url: 'https://upload.wikimedia.org/wikipedia/commons/thumb/7/74/Spotify_App_Logo.svg/2048px-Spotify_App_Logo.svg.png'
    }
  }
}
</script>

<style lang="scss" scoped>
  
</style>
