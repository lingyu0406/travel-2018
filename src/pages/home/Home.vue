<template>
  <div class="home">
    <home-header></home-header>
    <swiper></swiper>
    <home-btn></home-btn>
    <home-list></home-list>
  </div>
</template>

<script>
import HomeHeader from '@/home/components/Header.vue'
import Swiper from '@/home/components/Swiper.vue'
import HomeBtn from '@/home/components/HomeBtn.vue'
import HomeList from '@/home/components/HomeList.vue'
export default {
  name: 'Home',
  data () {
    return {
      
    }
  },
  components: {
  	HomeHeader,
  	Swiper,
  	HomeBtn,
  	HomeList
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
