<template>
  <div class="container">
      <div class="row row-cols-2 row-cols-sm-2 row-cols-md-6 disc-conteiner">
          <CardDisc v-for="(item, i) in Disc" :key="i" :img="item.poster" :title="item.title" :year="item.year" :author="item.author" :genere="item.genere" />
      </div>
  </div>
</template>

<script>
import CardDisc from './CardDisc.vue'
import axios from 'axios'

export default {
  name: 'ContentSpotify',
  data () {
    return {
      Disc: null
    }
  },
  components: {
    CardDisc
  },
  created () {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((response) => {
        this.Disc = response.data.response
      })
  }
}
</script>

<style lang="scss" scoped>
.disc-conteiner {
    display: flex;
    justify-content: center;
}
</style>
