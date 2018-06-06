<template>
  <div class="home-header">
    城市选择
    <div class="header-back" @click="goBack()"><span class="iconfont">&#xe624;</span></div>
  </div>
</template>

<script>
export default {
  name: 'CityHeader',
  data () {
    return {
      
    }
  },
  methods: {
  	goBack(){
  		this.$router.go(-1)
  	}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
	@import '../../../assets/css/varibals.styl'
	.home-header
		position relative
		width 100%
		height .88rem
		background $bgColor
		box-sizing border-box
		padding .12rem 0
		line-height .64rem
		font-size .34rem
		color #fff
		.header-back
			position absolute
			left .2rem
			top .12rem
		
</style>
