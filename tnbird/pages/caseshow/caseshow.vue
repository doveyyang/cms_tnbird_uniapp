<template>
	<view class="caseshow-container">
		<view class="content">
			<view class="item">
				<view class="pic">
					
					<scroll-view scroll-y>
						<view><image src="../../static/example/paper.jpg" mode="widthFix"></image></view>
					</scroll-view>
				</view>
				<view class="name">纸业微官网</view>
				<view class="tags">
					<view class="tag-item" >企业定制</view>
					<view class="tag-item" >地图导航</view>
					<view class="tag-item" >快捷通讯</view>					
				</view>
				<view class="desc">
					企业微官网拥有企业介绍、产品介绍、地图导航、实时通讯等功能的企业微门户小程序
				</view>
			</view>
			
			<view class="item">
				<view class="pic">
					
					<scroll-view scroll-y>
						<view><image src="../../static/example/16.png" mode="widthFix"></image></view>
					</scroll-view>
				</view>
				<view class="name">定蛋糕</view>
				<view class="tags">
					<view class="tag-item" >电商</view>
					<view class="tag-item" >支付</view>	
					<view class="tag-item" >预约</view>	
				</view>
				<view class="desc">
					在线定蛋糕具有了选蛋糕样式、预约下单、评论转发等功能
				</view>
			</view>
			<view class="item">
				<view class="pic">
					
					<scroll-view scroll-y>
						<view><image src="../../static/example/17.png" mode="widthFix"></image></view>
					</scroll-view>
				</view>
				<view class="name">稿小妹</view>
				<view class="tags">
					<view class="tag-item" >工具</view>
					<view class="tag-item" >定制</view>	
				</view>
				<view class="desc">
					稿小妹包含了预约，发稿，为书稿等文本管理定制解决方案
				</view>
			</view>
			<view class="item">
				<view class="pic">
					
					<scroll-view scroll-y>
						<view><image src="../../static/example/shop.jpg" mode="widthFix"></image></view>
					</scroll-view>
				</view>
				<view class="name">微商城</view>
				<view class="tags">
					<view class="tag-item" >电商</view>
					<view class="tag-item" >支付</view>	
				</view>
				<view class="desc">
					在线商城包含了用户注册、购物、提交订单、支付、商品管理、订单管理等功能
				</view>
			</view>
			<view class="item">
				<view class="pic">
					
					<scroll-view scroll-y>
						<view><image src="../../static/example/18.png" mode="widthFix"></image></view>
					</scroll-view>
				</view>
				<view class="name">车辆保洁服务</view>
				<view class="tags">
					<view class="tag-item" >会员</view>
					<view class="tag-item" >支付</view>	
					<view class="tag-item" >预约</view>	
					<view class="tag-item" >导航</view>	
				</view>
				<view class="desc">
					车辆保洁服务提供了会员注册、预约、导航、下单支付、营销推广等服务
				</view>
			</view>
			<view class="item">
				<view class="pic">
					
					<scroll-view scroll-y>
						<view><image src="../../static/example/phone.jpg" mode="widthFix"></image></view>
					</scroll-view>
				</view>
				<view class="name">手机维修</view>
				<view class="tags">
					<view class="tag-item" >支付</view>
					<view class="tag-item" >服务</view>	
					<view class="tag-item" >实时沟通</view>	
				</view>
				<view class="desc">
					手机维修平台提供了手机展示、修机拆机服务咨询、导航预约等功能
				</view>
			</view>
			
		</view>
	</view>
</template>

<script>
	import uniTag from "@/components/uni-tag/uni-tag.vue"
	export default {
		data() {
			return {
				
			};
		},
		methods:{
			returnback(){
				uni.navigateBack({
					delta:1
				})
			}
		},
		onLoad:function(option){
			uni.setNavigationBarTitle({
				title:'案例了解'
			})
			uni.setNavigationBarColor({
				frontColor:"#ffffff",
				backgroundColor:"#2c78ff",
				animation:{
					duration:100,
					timingFunc: 'easeIn'
				}
			})
		},
		components:{
			uniTag,
		}
		
	}
</script>

<style lang="scss">
	.caseshow-container{
		.content{
			display: flex;
			flex-wrap: wrap;
			padding:10upx;
			box-sizing: border-box;
			.item{
				width:345upx;
				min-height: 530upx;
				border: 1upx solid $uni-border-color;
				border-radius: 15upx;
				box-sizing: border-box;
				margin: 10upx;
				overflow: hidden;
				
				display: flex;
				flex-direction: column;
				
				.pic{
					height: 400upx;
					overflow: hidden;
					scroll-view {
						height: 400upx;
					}
					image{						
						height: 100%;
						width: 100%;						
					}
				}
				.name,.tags,.desc{
					padding: 10upx;
				}
				.name{
					font-size: $uni-font-size-lg;
					font-weight: 700;
					color: $uni-text-color;
				}
				
				.tags{
					display: flex;
					flex-wrap: wrap;
					justify-content:flex-start;
					
					.tag-item{
						box-sizing: border-box;
						display: inline-block;
						color: $uni-text-color;
						border-radius: $uni-border-radius-base;
						background-color: $uni-bg-color-grey;
						border: 1px solid $uni-bg-color-grey;
						height: 40upx;
						padding: 0px 16upx;
						line-height: calc(40upx - 2px);
						font-size: $uni-font-size-sm;
						margin: 5upx;
						border-radius: 30upx;
					}
					.tag-item:last-child, .tag-item:nth-last-child(2){
						margin-bottom:0;
					}
				}
				.desc{
					font-size: $uni-font-size-sm;
					color: $uni-text-color-grey;
				}
				
			}
		}
	}
</style>
