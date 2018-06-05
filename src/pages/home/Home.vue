<template>
  <div class="home">
    <home-header></home-header>
    <swiper></swiper>
    <home-btn></home-btn>
  </div>
</template>

<script>
import HomeHeader from '@/home/components/Header.vue'
import Swiper from '@/home/components/Swiper.vue'
import HomeBtn from '@/home/components/HomeBtn.vue'
export default {
  name: 'Home',
  data () {
    return {
      
    }
  },
  components: {
  	HomeHeader,
  	Swiper,
  	HomeBtn
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
