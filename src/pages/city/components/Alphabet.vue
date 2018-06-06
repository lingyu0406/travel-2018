<template>
	<div>
		<div class="list">
			<div class="list-item" v-for="(item,key) of city">{{key}}</div>
		</div>	
	</div>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
  	city: Object
  },
  data () {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
	@import '../../../assets/css/varibals.styl'
	.list
		position absolute
		top 1.68rem
		right 0
		bottom 0
		display flex
		flex-direction column
		justify-content center
		width .4rem
		.list-item
			color $bgColor
			line-height .4rem
			text-align center
		
</style>
