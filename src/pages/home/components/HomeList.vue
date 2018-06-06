<template>
  <div class="home-list">
	  <div class="home-hot">
	  	<div class="home-hot-title"><span class="iconfont hot-icon">&#xe658;</span>热门推荐</div>
		<div class="home-hot-list">
			<div class="hot-list-item" v-for="item of hotList" :key="item.id">
				<img class="list-img" :src="item.hotImg" alt="">
				<span class="list-title">{{item.title}}</span>
				<span class="list-price"><span class="orangeText">{{item.price}}</span>起</span>
			</div>
		</div>
	  </div>
	  <div class="home-guess">
	  	<div class="home-guess-title"><span class="iconfont guess-icon">&#xe601;</span>猜你喜欢</div>
		<div class="home-guess-list">
			<div class="guess-list-item" v-for="item of guessList" :key="item.id">
				<div class="list-img"><img class="list-img-content" :src="item.guessImg" alt=""></div>
				<div class="guess-list-text">
					<div class="vertical-center">
						<h3 class="list-title">{{item.title}}</h3>
						<p class="list-price"><span class="orangeText">{{item.price}}</span>起</p>
						<div class="list-comment-area">
							<p class="list-comment">{{item.comment}}条评论</p>
							<p class="list-area">{{item.area}}</p>
						</div>
					</div>
				</div>
			</div>
		</div>
	  </div>
	  <div class="home-weekend">
	  	<div class="home-weekend-title"><span class="iconfont weekend-icon">&#xe6c7;</span>周末去哪儿</div>
		<div class="weekend-list">
			<div class="weekend-list-item" v-for="item of weekendList" :key="item.id">
				<div class="list-item-img"><img class="list-item-img-content" :src="item.weekendImg" alt=""></div>
				<h3 class="list-title">{{item.title}}</h3>
				<p class="list-desc">{{item.description}}</p>
			</div>
		</div>
	  </div>
  </div>
</template>

<script>
export default {
  name: 'HomeList',
  data () {
    return {
      hotList: [
	    {
	    	'id': '001',
	    	'hotImg': 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_150x150_06cb3e52.jpg',
	    	'title': '颐和园',
	    	'price': '65元'
	    },
	    {
	    	'id': '002',
	    	'hotImg': 'http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_150x150_2dec3e78.jpg',
	    	'title': '故宫',
	    	'price': '85元'
	    },
	    {
	    	'id': '003',
	    	'hotImg': 'http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_200x200_0938a8f2.jpg',
	    	'title': '圆明园',
	    	'price': '25元'
	    },
	    {
	    	'id': '004',
	    	'hotImg': 'http://img1.qunarzz.com/sight/p0/1804/c8/c88bb5e69c9a9c5ea3.img.jpg_200x200_740720ff.jpg',
	    	'title': '朝阳公园',
	    	'price': '25元'
	    },{
	    	'id': '005',
	    	'hotImg': 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_150x150_06cb3e52.jpg',
	    	'title': '天安门',
	    	'price': '1元'
	    }
      ],
      guessList: [
      	{
      		'id': '001',
	    	'guessImg': 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_150x150_06cb3e52.jpg',
	    	'title': '圆明园',
	    	'price': '25元',
	    	'comment': '2043',
	    	'area': '海淀区'
      	},
      	{
      		'id': '002',
	    	'guessImg': 'http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_150x150_2dec3e78.jpg',
	    	'title': '颐和园',
	    	'price': '65元',
	    	'comment': '4043',
	    	'area': '海淀区'
      	},
      	{
      		'id': '003',
	    	'guessImg': 'http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_200x200_0938a8f2.jpg',
	    	'title': '朝阳公园',
	    	'price': '25元',
	    	'comment': '43',
	    	'area': '朝阳'
      	},
      	{
      		'id': '004',
	    	'guessImg': 'http://img1.qunarzz.com/sight/p0/1804/c8/c88bb5e69c9a9c5ea3.img.jpg_200x200_740720ff.jpg',
	    	'title': '古北水镇',
	    	'price': '25元',
	    	'comment': '2043',
	    	'area': '密云县'
      	}
      ],
      weekendList: [
      	{
      		'id': '001',
	    	'weekendImg': 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
	    	'title': '寻找北京的皇城范儿',
	    	'description': '数百年的宫廷庙宇，至今依旧威严霸气'
      	},
      	{
      		'id': '002',
	    	'weekendImg': 'http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg',
	    	'title': '北京必游TOP10',
	    	'description': '来北京必去的景点非这些地方莫属'
      	},
      	{
      		'id': '003',
	    	'weekendImg': 'http://img1.qunarzz.com/sight/source/1505/ce/bc89bc2f0e33ea.jpg_r_640x214_3e408453.jpg',
	    	'title': '学生最爱的博物馆',
	    	'description': '周末干嘛？北京很多博物馆已经免费开放啦'
      	},
      	{
      		'id': '004',
	    	'weekendImg': 'http://img1.qunarzz.com/sight/source/1505/b2/fde1bfcd057a52.jpg_r_640x214_bbf3fa44.jpg',
	    	'title': '儿童剧场，孩子的乐园',
	    	'description': '带宝贝观看演出，近距离体验艺术的无穷魅力'
      	},
      	{
      		'id': '005',
	    	'weekendImg': 'http://img1.qunarzz.com/sight/source/1507/18/2d554e22faa25f.jpg_r_640x214_2a966a54.jpg',
	    	'title': '爱上庄园',
	    	'description': '庄园让臭美的你秒变白富美，高富帅'
      	}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
	@import '../../../assets/css/varibals.styl'
	.home-list
		margin-top .1rem
		.home-hot-title,
		.home-guess-title,
		.home-weekend-title
			background #eee
			line-height .44rem
			padding .05rem .2rem
			text-align left
			.iconfont
				padding-right .1rem
			.hot-icon
				color red
			.guess-icon 
				color #fc542d
			.weekend-icon
				color #1bae6e
		.home-hot-list
			padding .2rem
			overflow-x scroll
			box-sizing border-box
			white-space nowrap
			width 100%
			.hot-list-item
				width 28%
				display inline-block
				height auto
				margin-right .1rem
				.list-img
					width 100%
					display block
					margin-bottom .16rem
				.list-title
				.list-price
					display block
					line-height 1.5
					.orangeText
						color #f09a12
						margin-right .07rem
		.home-guess-list
			padding .2rem .2rem 0 .2rem
			.guess-list-item
				display flex
				justify-content space-between
				margin-bottom .2rem
				.list-img					
					width 40%
					margin-bottom .16rem
					.list-img-content
						width 100%
						display block
				.vertical-center
					width 100%
				.guess-list-text
					flex 2
					text-align left
					display flex
					align-items center
					margin-left .2rem
					.list-title
						font-size .36rem
						margin-bottom .2rem
					.list-price
						display block
						margin-bottom .2rem
						.orangeText
							color #f09a12
							margin-right .07rem
							font-size .44rem
					.list-comment-area
						display flex
						justify-content space-between
						.list-comment
							color #999
							font-size .22rem
							flex 1
						.list-area
							color $darkTextColor
							text-align right
							font-size .24rem
		.weekend-list-item
			margin-bottom .2rem
			.list-item-img
				overflow hidden
				width 100%
				height 0
				padding-bottom 34%
				margin-bottom .1rem
				.list-item-img-content
					width 100%
			.list-title
				margin-left .2rem
				line-height .44rem
				text-align left
			.list-desc				
				margin-left .2rem
				line-height .44rem
				text-align left
				font-size .22rem
				color #666
			
</style>
