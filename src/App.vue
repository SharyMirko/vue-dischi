<template>
  <div id="app">
    <HeaderSpotify :arrType="arrType" :arrAuth="arrAuth" @customChange="change($event)" @author="authorChange($event)" />
    <ContentSpotify :author="author" :type="type" @allobj="arrAuthPopol($event)" />
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
      type: '',
      author: '',
      arrAuth: [],
      arrType: []
    }
  },
  components: {
    FooterSpotify,
    ContentSpotify,
    HeaderSpotify
  },
  methods: {
    authorChange (i) {
      this.author = i
    },
    change (i) {
      this.type = i
    },
    arrAuthPopol (info) {
      setTimeout(info.forEach(disc => {
        this.arrAuth.push(disc.author)
        if (this.arrType.includes(disc.genre)) {
          console.log('s')
        } else {
          this.arrType.push(disc.genre)
        }
      }), 3000)
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
