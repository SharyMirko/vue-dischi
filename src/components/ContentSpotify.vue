<template>
  <div class="container">
      <div class="disc-conteiner">
          <CardDisc />
      </div>
  </div>
</template>

<script>
import CardDisc from './CardDisc.vue'
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
  }
}
</script>

<style lang="scss" scoped>
.disc-conteiner {
    display: flex;
    justify-content: center;
}
</style>
