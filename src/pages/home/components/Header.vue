<template>
  <div class="home-header">
    <div class="header-back"><span class="iconfont">&#xe624;</span></div>
    <div class="header-search"><span class="iconfont">&#xe632;</span>输入您要搜索的主题</div>
    <router-link tag="div" class="header-city" to="/city">北京<span class="iconfont">&#xe600;</span></router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  data () {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
	@import '../../../assets/css/varibals.styl'
	.home-header
		width 100%
		height .88rem
		background $bgColor
		display flex
		justify-content space-between
		box-sizing border-box
		padding .12rem .2rem
		line-height .64rem
		color #fff
		.header-back
			padding-right .2rem;
		.header-search
			flex 1
			box-sizing border-box
			padding 0 .1rem
			background #fff
			border-radius .08rem
			color #ccc
			text-align left
		.header-city
			padding-left .2rem
			box-sizing border-box
			min-width .44rem
</style>
