<template>
  <div id="app">
    <HeaderSpotify />
    <FooterSpotify />
    <ContentSpotify />
  </div>
</template>

<script>
import HeaderSpotify from './components/HeaderSpotify.vue'
import FooterSpotify from './components/FooterSpotify.vue'
import ContentSpotify from './components/ContentSpotify.vue'

export default {
  name: 'App',
  components: {
    HeaderSpotify,
    FooterSpotify,
    ContentSpotify
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
body {
  background-color: #2E3A46;
}
</style>
