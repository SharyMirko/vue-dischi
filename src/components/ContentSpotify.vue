<template>
  <div class="container">
    <p v-if="Disc == null">Dati in caricamento</p>
      <div v-else class="row row-cols-2 row-cols-sm-2 row-cols-md-6 disc-conteiner">
          <CardDisc v-for="item in display" :key="item.title" :img="item.poster" :title="item.title" :year="item.year" :author="item.author" :genre="item.genre" />
      </div>
  </div>
</template>

<script>
/* eslint-disable */
import CardDisc from './CardDisc.vue'
import axios from 'axios'

export default {
  name: 'ContentSpotify',
  data () {
    return {
      Disc: null,
      arrAuth: null
    }
  },
  props: {
    type: String,
    author: String
  },
  computed: {
    display () {
     return this.Disc.filter(obj => obj.genre.includes(this.type) && obj.author.includes(this.author))
    }
  },
  components: {
    CardDisc,
  },
  created () {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((response) => {
        this.Disc = response.data.response
      }).then((Disc) => { this.$emit('allobj', this.Disc)})
  }
}
</script>

<style lang="scss" scoped>
.disc-conteiner {
    display: flex;
    justify-content: center;
}
</style>