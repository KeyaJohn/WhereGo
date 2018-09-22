<template>
  <div>
    <Header></Header>
    <Swiper></Swiper>
  </div>
</template>

<script>
import Header from './components/Header'
import Swiper from './components/Swiper'
export default {
  name: 'Home',
  components: {
    Header: Header,
    Swiper: Swiper
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
