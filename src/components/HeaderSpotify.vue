<template>
<header class="container-fluid">
   <div class="logo"><img src="../assets/img/logo-small.svg" alt=""></div>
   <div class="selection">
       <select name="selection" id="selection">
           <option value="all">All</option>
           <option value="all">All</option>
           <option value="all">All</option>
           <option value="all">All</option>
       </select>
   </div>
</header>
</template>

<script>
export default {

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
