<template>
  <div class="search-wraper">
    <input class="search-input" v-model="keyword" type="text" placeholder="请输入要搜索的城市">
    <div class="search-content" v-show="keyword" ref="search">
        <div>
          <div class="search-item border-topbottom" v-for="item in list">{{item.name}}</div>
          <div class="search-item border-topbottom" v-show="!list.length">没有匹配到数据</div>            
        </div>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'Search',
  props: {
    city: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  watch: {
    keyword(){
        if(this.timer){
            clearTimeout(this.timer)
        }
        this.timer = setTimeout(()=>{
            let result = [];
            for(let i in this.city){
                this.city[i].forEach((item) => {
                    if(item.spell.indexOf(this.keyword) > -1 || item.name.indexOf(this.keyword) > -1){
                        result.push(item)
                    }
                })
            this.list = result
            }
        }, 100);
    }
  },
  mounted(){
    this.scroll = new BScroll(this.$refs.search)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
  @import '../../../assets/css/varibals.styl'
  .search-wraper
    background $bgColor
    padding .1rem .2rem .2rem
    .search-input
      width 100%
      border-radius .3rem
      line-height .34rem
      padding .1rem .2rem
      box-sizing border-box
      text-align center
    .search-content
      overflow hidden
      background-color #f5f5f5
      position absolute
      top 1.68rem
      left 0
      right 0
      bottom 0
      z-index 1
      .search-item
          line-height .64rem
          padding 0 .2rem
          text-align left
          background-color #fff
     
    	
</style>
