<template>
  <div class="home-btn-wrap">
	<div class="home-btn">
		<div class="home-btn-img">
			<img class="btn-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png" alt="">
			<div class="home-btn-title">景点门票</div>
		</div>
	</div>
	<div class="home-btn">
		<div class="home-btn-img">
			<img class="btn-img-content" src="http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png" alt="">
			<div class="home-btn-title">景点门票</div>
		</div>
	</div>
	
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
	.home-btn-wrap
		overflow hidden
		width 100%
		height 0
		padding-bottom 50%
		margin-top .2rem
		.home-btn
			position: relative
			width 25%
			padding-bottom 25%
			float left
			.home-btn-img 
				position absolute
				left 0
				top 0
				right 0
				bottom .44rem
				.btn-img-content 
					height 100%
					display block
					margin 0 auto
				.home-btn-title
					color $darkTextColor
					font-size .28rem
			
</style>
