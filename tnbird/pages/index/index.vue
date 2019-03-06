<template>
	<view class="index-container">
		<swiper class="swiper" :indicator-dots="true" :autoplay="true" :interval="10000" :duration="1000" indicator-color="#ffffff" indicator-active-color="#f1f1f1">
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
				{image:'../../static/func/case.png',text:'案例了解',ntext:'行业/功能',width:42,height:42,style:'position:absolute;'},
				{image:'../../static/func/services.png',text:'定制服务',ntext:'品牌/业务',width:45,height:52,style:'position:absolute;margin-top:-4px'},
				{image:'../../static/func/market.png',text:'市场优势',ntext:'用户/渠道',width:60,height:55,style:'position:absolute;margin-left:-8px;margin-top:-5px'}]" 
				column-num="3" @click="gotoPageIndex" showBorder="false" >
			</uni-grid> 
		</view>
		
		<view class="noticeBar">
			 <uni-notice-bar 
				@getmore="getMore" 
				show-icon="true" 
				speed="60"
				single="true" 
				scrollable='true'
				text="图南鸟科技团队全栈定制服务开启,欢迎您咨询">
			</uni-notice-bar>
		</view>
		<!-- 产品推荐 -->
		<view class="uni-card product-hot">
			<view class="uni-card-header">
					产品推荐
			</view>
			<view class="uni-card-content">
				<view class="uni-card-content-inner" @click="goService">
					<view class="content">					
						 <view class="pro-left">
							 Web网站建设
							 <view class="pro-left-text">让用户更容易搜索到</view>
						 </view>
						 <view class="pro-right">
						 	<view class="top">
								Html5小程序
								<view class="pro-left-text">即用即走,用户热衷</view>
							</view>
						 	<view class="bottom">
								APP软件开发
								<view class="pro-left-text">长期锁住用户，增加回购</view>
							</view>
						 </view>
					</view>
				</view>
			</view>
		</view>
		<!-- 案例一览 -->
		<view class="uni-card example" @click="gotoshowPage">
			<view class="uni-card-header">
					案例一览
					<view class="uni-card-header-extra" @click.stop="gotoshowPage">查看更多</view>
			</view>
			<view class="content">								
				 <view class="content-item ">
					 <image src="../../static/example/shop.jpg" ></image>
					 <view class="btn-detail"> 订单交易 </view>
				 </view>
				 <view class="content-item ">
					<image src="../../static/example/paper.jpg" ></image>
					<view class="btn-detail"> 官网展示 </view>
					 </view>
				 <view class="content-item ">
					<image src="../../static/example/phone.jpg" ></image>
					<view class="btn-detail"> 生活服务 </view>
				 </view>
			</view>
		</view>
		
		<!-- 联系我们 -->
		<view class="contact" @click="gotoContactPage">
			<view class="contact-way">				
			</view>
		</view>
		
		<!-- 为了兼容IOS，显示扩高20upx -->
		<view class="empty " style="height: 20upx;"></view>
	</view>
</template>

<script>
	import uniGrid from '@/components/uni-grid/uni-grid.vue'
	import uniNoticeBar from "@/components/uni-notice-bar/uni-notice-bar.vue"
	import uniCard from '@/components/uni-card/uni-card.vue'
	export default {
		data() {
			return {
			}
		},
		onLoad() {
			uni.setNavigationBarTitle({
				title:'图南鸟网络科技'
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
		methods: {
			goService(){
				uni.navigateTo({
					url:'../services/services'
				})
			},
			getMore(){
				console.log('getMore');
			},
			gotoshowPage(){
				uni.navigateTo({
					url:'../caseshow/caseshow'
				});
			},
			gotoContactPage(){
				uni.navigateTo({
					url:"../contactus/contactus"
				})
			},
			gotoPageIndex(e){
				console.log(e);
				switch(e.index){
					case 0:
						uni.navigateTo({
							url:'../caseshow/caseshow'
						});
						break;
					case 1:uni.navigateTo({
							url:'../services/services'
						});
						break;

					case 2:uni.navigateTo({
							url:'../advantages/advantages'
						})
						break;
				}
			}
		},
		components:{
			uniGrid,uniNoticeBar,uniCard
		}
	}
</script>

<style lang="scss">
	.index-container{
		background-color: $uni-bg-color;
		// 轮播图
		.swiper{
			height: 400upx;
			width: 750upx;
			.swiper-item{
				image{
					width: 100%;
					height: 100%;
				}
			}
		}
		
		// 功能选项
		.grid-content{
			margin: $uni-spacing-col-lg $uni-spacing-row-base;
			// border: 1px solid $uni-border-color;
			// border-radius: $uni-border-radius-lg;
			// box-shadow:  0 10upx 0 $uni-border-color;
			
			
		}
		
		//通告栏
		.noticeBar{
			margin: 0 $uni-spacing-row-sm;
			// border:1px solid $uni-border-color;
			border-radius: 30upx;
			overflow: hidden;
		}
		
		// 产品推荐
		.product-hot{			
			margin-top: $uni-spacing-row-sm;
			.uni-card-header{
				margin: 20upx 0;
				 font-size:$uni-font-size-lg;
				 font-weight: 700;
				 border-left: 3px solid #0eb2fe;
				 line-height: 40upx;
				 padding-left: 20upx;
			 }
			 
			.content{
				height: 320upx;
				display: flex;
				.pro-left{
					height: 100%;
					width: 50%;
					background-color: #fbfbfb;
					box-sizing: border-box;
					border-radius: 20upx;
					padding: 10upx;
					font-size: $uni-font-size-base;
					background: url('../../static/product/web.png') no-repeat ;
					background-size: 375upx 320upx;
					&-text{
						font-size: $uni-font-size-sm;
						color: $uni-text-color-grey;
					}
				}
				.pro-right{
					display: flex;
					flex-direction: column;
					height: 100%;
					width: 50%;
					margin-left: 10upx;
					.top{
						height: 160upx;
						background-color: #fbfbfb;
						box-sizing: border-box;
						border-radius: 20upx;
						padding: 10upx;
						font-size: $uni-font-size-base;
						background: url('../../static/product/html.png') no-repeat ;
						background-size: 375upx 160upx;
					}
					.bottom{
						margin-top: 10upx;
						height: 160upx;
						background-color: #fbfbfb;
						box-sizing: border-box;
						border-radius: 20upx;
						padding: 10upx;
						font-size: $uni-font-size-base;
						background: url('../../static/product/app.png') no-repeat ;
						background-size: 375upx 160upx;
					}
				}
			}
		}
		
		// 案例一览  
		.example{
			margin-top: $uni-spacing-row-sm;
			.uni-card-header{
				margin: 20upx 0;
				 font-size:$uni-font-size-lg;
				 font-weight: 700;
				 border-left: 3px solid #0eb2fe;
				 line-height: 40upx;
				 padding-left: 20upx;
				 position: relative;
				 .uni-card-header-extra{
					 position: absolute;
					 right: 10upx;
					 top: 0;
					 font-size:$uni-font-size-base;
					 font-weight: 400;
					 color:#0eb2fe
				 }
				 .uni-card-header-extra:after{
					 content: '>';
					 line-height:$uni-font-size-base;
					 padding-left: 5upx;
				 }
			 }
			 .content{
			 	display: flex;
			 	justify-content: space-between;
				
				
				&-item{
					height: 400upx;
					width: 32%;
					position: relative;
					color: #ffffff;
					// border: 1px solid red;
					// overflow: hidden;
					image{
						width: 100%;
						height: 100%;
						vertical-align: middle;
						// border: 1px solid blue;
					}
					
					.btn-detail{
						
						position: absolute;
						bottom: 0;
						left: 0;
						height: 50upx;
						width: 100%;
						background: #47c4fe no-repeat;
						opacity: .8;
						border-radius: 0 0 10upx 10upx;
						line-height: 50upx;
						padding-left:15upx; 
						box-sizing: border-box;
						font-size: $uni-font-size-base;

					}
					.btn-detail:after{
						content: "详情>";
						right: 10upx;
						// padding-right: 10upx;
						font-size: $uni-font-size-sm;
						position: absolute;
						line-height: 50upx;
					}
					
				}
			 }
		}
	
		//联系我们
		.contact{
			margin:50upx 0;
			height: 350upx;
			width: 100%;
			background: url('../../static/contact/contactus.jpg') no-repeat;
			
			background-size: 100% 100%;
			
			.contact-way{
				position: fixed;
				right: 20upx;
				bottom: 300upx;
				width: 120upx;
				height: 120upx;
				background:url('../../static/contact/contact-text.png') 35upx 35upx no-repeat ;
				background-size: 50upx,50upx;
				background-color: $uni-bg-color;
				border-radius: 50%;
				
			}
		}
	}
</style>
