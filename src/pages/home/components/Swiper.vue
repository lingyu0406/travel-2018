<template>
  <div class="home-swiper">
    <swiper class="swiper" :options="swiperOption" ref="mySwiper">
	    <!-- slides -->
	    <swiper-slide><img class="swiper-img" src="http://img1.qunarzz.com/piao/fusion/1805/b6/2330c92270c7e802.jpg_750x200_425e2121.jpg" alt=""></swiper-slide>
	    <swiper-slide><img class="swiper-img" src="http://img1.qunarzz.com/piao/fusion/1805/e5/59fad13a64807d02.jpg_750x200_713ae984.jpg" alt=""></swiper-slide>
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
        }
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
