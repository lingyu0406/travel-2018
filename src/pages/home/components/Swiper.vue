<template>
  <div class="home-swiper">
    <swiper class="swiper" :options="swiperOption" ref="mySwiper">
	    <!-- slides -->
	    <swiper-slide v-for="item of swiperImgs" :key="item.id"><img class="swiper-img" :src="item.img" alt=""></swiper-slide>
	    <!-- Optional controls -->
	    <div class="swiper-pagination"  slot="pagination"></div>
	  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  data () {
    return {
      	swiperOption: {
          pagination: {
            el: '.swiper-pagination'
          },
          loop: true,
          autoplay: true
        },
        swiperImgs: [
        	{
        		'id': '001',
        		'img': 'http://img1.qunarzz.com/piao/fusion/1805/e5/59fad13a64807d02.jpg_750x200_713ae984.jpg'
        	},
        	{
        		'id': '002',
        		'img': 'http://img1.qunarzz.com/piao/fusion/1805/3b/ef86879aa50e3002.jpg_750x200_2a108508.jpg'
        	},
        	{
        		'id': '003',
        		'img': 'http://img1.qunarzz.com/piao/fusion/1806/1c/4847ea66072c7b02.jpg_750x200_c32457fb.jpg'
        	},
        	{
        		'id': '004',
        		'img': 'http://img1.qunarzz.com/piao/fusion/1804/bd/8e4a1c3f470d3702.jpg_750x200_f1f0a8c7.jpg'
        	}
        ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
	.home-swiper >>> .swiper-pagination-bullet-active
		background #fff 
	.home-swiper
		overflow hidden
		width 100%
		height 0
		padding-bottom 26.67%
		background #ccc
		.swiper
			overflow hidden
			width 100%
			height 0
			padding-bottom 26.67%
			.swiper-img
				width 100%
</style>
