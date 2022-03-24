<template>
  <div class="col special">
      <img :src="img" alt="">
      <span class="title">{{title}}</span>
      <span class="text">{{author}}</span>
      <span class="text">{{year}}</span>
  </div>
</template>

<script>
export default {
  name: 'CardDisc',
  props: {
    author: String,
    genere: String,
    img: String,
    title: String,
    year: String
  }
}
</script>

<style lang="scss" scoped>
.special {
  background-color: #2E3A46;
  margin: .5rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1.8rem;
  img {
    width: 10rem;
    height: 10rem;
  }
}
.title {
  font-size: 1.3rem;
  font-weight: bold;
  color: #fff;
  text-align: center;
}
  .text {
    color: #727A7D;
  }
  span {
    margin: .3rem
  }
</style>
