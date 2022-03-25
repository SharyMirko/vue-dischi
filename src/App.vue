<template>
  <div id="app">
    <HeaderSpotify @customChange="change($event)" />
    <ContentSpotify :type="type" />
    <FooterSpotify />
  </div>
</template>

<script>
import FooterSpotify from './components/FooterSpotify.vue'
import ContentSpotify from './components/ContentSpotify.vue'
import HeaderSpotify from './components/HeaderSpotify.vue'

export default {
  name: 'App',
  data () {
    return {
      type: ''
    }
  },
  components: {
    FooterSpotify,
    ContentSpotify,
    HeaderSpotify
  },
  methods: {
    change (i) {
      this.type = i
    }
  }
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
body {
  background-color: #1E2D3B;
}
</style>
