<template>
  <div class="city">
  	<city-header></city-header>
    <search :city="city"></search>
    <list :hotCity="hotCity" :city="city"></list>
    <alphabet :city="city"></alphabet>
  </div>
</template>

<script>
import CityHeader from '@/city/components/Header.vue'
import Search from '@/city/components/Search.vue'
import List from '@/city/components/List.vue'
import Alphabet from '@/city/components/Alphabet.vue'
import axios from 'axios'
export default {
  name: 'City',
  data () {
    return {
      hotCity: [],
      city: {}
    }
  },
  components: {
  	CityHeader,
    Search,
    List,
    Alphabet
  },
  methods: {
    fetchData(){
      axios.get('/api/city.json')
      .then(this.fetchDataSucc)
    },
    fetchDataSucc(res){
      const data = res.data.data
      this.hotCity = data.hotCities
      this.city = data.cities
    }    
  },
  mounted(){
    this.fetchData()
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
	.city
		background #f5f5f5
</style>
