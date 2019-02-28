<template>
	<view class="services-container">
		<image src="../../static/services/services.png" mode="widthFix"></image>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		onLoad() {
			uni.setNavigationBarTitle({
				title:"定制服务"
			})
			uni.setNavigationBarColor({
				frontColor:"#ffffff",
				backgroundColor:"#2c78ff",
				animation:{
					duration:100,
					timingFunc: 'easeIn'
				}
			})
		}
	}
</script>

<style lang="scss">
	.services-container{
		image{
			width:100%;
		}
	}
</style>
