<template>
	<view class="adv-container">
		<image src="../../static/advantages/advs.png" mode="widthFix"></image>
		<image src="../../static/advantages/desc.png" mode="widthFix"></image>
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
				title:"市场优势"
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
.adv-container{
	background-color: #fafafa;
	image{
		width: 100%;
	}
}
</style>
