<template>
<header class="container-fluid">
   <div class="logo"><img src="../assets/img/logo-small.svg" alt=""></div>
   <div class="selection">
       <select @change="$emit('customChange', genere)" v-model="genere" name="selection" id="selection">
           <option value="">All</option>
           <option value="Metal">Metal</option>
           <option value="Pop">Pop</option>
           <option value="jazz">Jazz</option>
           <option value="rock">Rock</option>
       </select>
   </div>
</header>
</template>

<script>

export default {
  name: 'HeaderSpotify',
  data () {
    return {
      genere: ''
    }
  }
}
</script>

<style lang="scss" scoped>
header {
    background-color: #2E3A46;
    height: 5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: .5rem 1rem;
    .logo img {
        width: 3.5rem
    }
    #selection {
        margin-right: 1rem;
    }
}
</style>
