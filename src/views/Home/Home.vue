<template>
  <div class="home">
    <NavBar class="nav-bar">
      <div class="center" slot="center">
        <img src="https://www.rakuten.ne.jp/gold/fedonline/images/huang.png">
      </div>
    </NavBar>
    <carousel class="carousel"></carousel>
  </div>
</template>

<script>
import NavBar from '@/components/navbar/NavBar.vue'
import carousel from './children/carousel'
export default {
  name: 'Home',
  components: {
    NavBar,
    carousel
  }
}
</script>
<style scoped>
  .nav-bar {
    background-color: #000;
  }
  .nav-bar .center img {
    width: 70px;
    margin-top: 5px;
  }
</style>
