<template>
	<view class="index-container">
		<swiper class="swiper" :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000" indicator-color="#ffffff" indicator-active-color="#f1f1f1">
			<swiper-item >
				<view class="swiper-item"><image src="../../static/banner/banner.jpg" mode="widthFix"></image></view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item"><image src="../../static/banner/banner.jpg" mode="widthFix"></image></view>
			</swiper-item>
			<swiper-item>
				<view class="swiper-item"><image src="../../static/banner/banner.jpg" mode="widthFix"></image></view>
			</swiper-item>
		</swiper>
		
		<view class="grid-content">
			<uni-grid :data="[
				{image:'../../static/func/example1.jpg',text:'案例了解',ntext:'行业/功能'},
				{image:'../../static/func/example1.jpg',text:'定制服务',ntext:'品牌/业务'},
				{image:'../../static/func/example1.jpg',text:'市场优势',ntext:'用户/渠道'}]" 
				column-num="3">
			</uni-grid>
		</view>
		
		<view class="noticeBar">
			<uni-notice-bar 
				show-icon="true" 
				single="true" 
				text="图南鸟科技团队全栈定制服务开启,欢迎您咨询" color="#666666" background-color="#fff">
			</uni-notice-bar>
		</view>
	</view>
</template>

<script>
	import uniGrid from '@/components/uni-grid/uni-grid.vue'
	import uniNoticeBar from "@/components/uni-notice-bar/uni-notice-bar.vue"
	export default {
		data() {
			return {
			}
		},
		onLoad() {

		},
		methods: {

		},
		components:{
			uniGrid,uniNoticeBar
		}
	}
</script>

<style lang="scss">
	.index-container{
		background-color: $uni-bg-color;
		.swiper{
			height: 400upx;
			width: 750upx;
			.swiper-item{
				// width: 750upx;
				// overflow:hidden;
				
				
				// border: 1upx solid red;
				image{
					width: 100%;
					height: 100%;
					// height: 100%;
					// vertical-align:bottom;
				}
			}
		}
		
		.grid-content{
			margin: $uni-spacing-col-lg $uni-spacing-row-base;
			border: 1px solid $uni-border-color;
			border-radius: $uni-border-radius-lg;
		}
		
		.noticeBar{
			margin: 0 $uni-spacing-row-sm;
		}
	}
</style>
