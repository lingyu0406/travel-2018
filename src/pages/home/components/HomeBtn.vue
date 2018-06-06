<template>
  <div class="home-btn-wrap">
  	<swiper class="swiper" ref="mySwiper">
		<swiper-slide v-for = "(page, index) of pages" :key="index">
			<div class="home-btn" v-for="item in page">
				<div class="home-btn-img">
					<img class="btn-img-content" :src="item.swiperImg" alt="">
					<div class="home-btn-title">{{item.title}}</div>
				</div>
			</div>
		</swiper-slide>
	</swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeBtn',
  data () {
    return {
      swiperList: [
      	{
      		'id': '001',
      		'swiperImg': 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
      		'title': '景点门票'
      	},
      	{
      		'id': '002',
      		'swiperImg': 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
      		'title': '景点门票'
      	},
      	{
      		'id': '003',
      		'swiperImg': 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
      		'title': '景点门票'
      	},
      	{
      		'id': '004',
      		'swiperImg': 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
      		'title': '景点门票'
      	},
      	{
      		'id': '005',
      		'swiperImg': 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
      		'title': '景点门票'
      	},
      	{
      		'id': '006',
      		'swiperImg': 'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
      		'title': '景点门票'
      	},
      	{
      		'id': '007',
      		'swiperImg': 'http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png',
      		'title': '景点门票'
      	},
      	{
      		'id': '008',
      		'swiperImg': 'http://img1.qunarzz.com/piao/fusion/1804/ed/cf572be30fc32f02.png',
      		'title': '景点门票'
      	},
      	{
      		'id': '009',
      		'swiperImg': 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
      		'title': '景点门票'
      	}
      ]
    }
  },
  computed: {
  	pages(){
  		const pages = []
  		this.swiperList.forEach( (item, index) => {
  			const page = Math.floor(index / 8)
  			if(!pages[page]){
  				pages[page] = []
  			}
  			pages[page].push(item)
  		});
  		return pages
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
					box-sizing border-box
					padding .1rem 
					height 100%
					display block
					margin 0 auto
				.home-btn-title
					color $darkTextColor
					font-size .24rem     
			
</style>
