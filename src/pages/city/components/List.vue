<template>
  <div class="city-list" ref="wrapper">
   <div class="content">
     <div class="hot-city-title">热门城市</div>
      <ul class="cities">
        <li @click="handleClick(item.name)" v-for="item of hotCity" :key="item.id">{{item.name}}</li>
      </ul>
      <div class="city-list-wrap" v-for="(item,key) of city" :key="key" :ref="key">
        <div class="list-title">{{key}}</div>
        <div class="list-content" v-for="innerItem of item" @click="handleClick(innerItem.name)">
          <div class="list-item">{{innerItem.name}}</div>
        </div>
      </div>
   </div>
       
  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  props: {
    hotCity: Array,
    city: Object,
    letter: String
  },
  watch: {
    letter(){
      if(this.letter){
        let el = this.$refs[this.letter][0]
        this.scroll.scrollToElement(el)
      }
    }
  },
  methods: {
    handleClick(city){
      this.$store.commit('changeCity',city)
      this.$router.push('/')
    }
  },
  mounted(){
    this.scroll = new BScroll(this.$refs.wrapper,{click:true})
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
  @import '../../../assets/css/varibals.styl'
  .city-list
    background-color #f5f5f5
    text-align left
    overflow hidden
    position absolute
    left 0
    top 1.68rem
    bottom 0
    right 0
    .hot-city-title
      line-height .64rem
      padding 0 .2rem
    .cities
      overflow hidden
      background #fff
      padding .1rem .2rem
      li
        width 33.3333%
        float left
        text-align center
        line-height .64rem
    .list-title
      line-height .64rem
      padding 0 .2rem
    .list-content
      padding .1rem .2rem
      background #fff
      .list-item
        line-height .64rem
		
</style>
