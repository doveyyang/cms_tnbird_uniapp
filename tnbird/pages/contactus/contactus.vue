<template>
	<view class="contact-container">
		<view class="banner">
			<image src="../../static/contact/title.png" mode="widthFix"></image>
		</view>
		<view class="team">
			<view class="title">靠谱的团队</view>
			<view class="desc">图南鸟网络科技是一个集市场销售，互联网技术、设计运营组成的自主研发销售运营互联网产品的企业。为客户提供网站建设、小程序、app定制、logo设计、营销运营等服务</view>
			<view class="pic">
				<image src="../../static/contact/team.png" mode="widthFix"></image>
			</view>
		</view>
		
		<view class="values">
			<image src="../../static/contact/value.png" mode="widthFix"></image>
		</view>
		
		<view class="info">
			<view class="title">核心成员</view>
			<view class="cards">
				<view class="card">
					<view class="info">						
						<view class="name">
							Brad
							<view class="name-desc">业务部</view>
						</view>
						<view class="phone">
							联系电话:
							<view class="phone-desc">135 5080 7080</view>
						</view>
						<view class="email">
							电子邮箱:
							<view class="email-desc">BradPitt@tnbird.com</view>
						</view>
						<view class="address">
							通讯地址:四川省绵阳市电商谷212室
						</view>
					</view>
					<view class="avertar">
						<image src="../../static/contact/avertar.png"></image>
					</view>
				</view>
				
				<view class="card">
					<view class="info">						
						<view class="name">
							Dovey
							<view class="name-desc">技术部</view>
						</view>
						<view class="phone">
							联系电话:
							<view class="phone-desc">180 1062 0509</view>
						</view>
						<view class="email">
							电子邮箱:
							<view class="email-desc">DoveyYang@tnbird.com</view>
						</view>
						<view class="address">
							通讯地址:四川省绵阳市电商谷212室
						</view>
					</view>
					<view class="avertar">
						<image src="../../static/contact/avertar.png"></image>
					</view>
				</view>
				<view class="card">
					<view class="info">						
						<view class="name">
							雨舸
							<view class="name-desc">设计部</view>
						</view>
						<view class="phone">
							联系电话:
							<view class="phone-desc">180 1062 0509</view>
						</view>
						<view class="email">
							电子邮箱:
							<view class="email-desc">liaoyuge@tnbird.com</view>
						</view>
						<view class="address">
							通讯地址:四川省绵阳市电商谷212室
						</view>
					</view>
					<view class="avertar">
						<image src="../../static/contact/avertar.png"></image>
					</view>
				</view>
				<view class="card">
					<view class="info">						
						<view class="name">
							Shero
							<view class="name-desc">UI设计师</view>
						</view>
						<view class="phone">
							联系电话:
							<view class="phone-desc">180 1062 0509</view>
						</view>
						<view class="email">
							电子邮箱:
							<view class="email-desc">liaomin@tnbird.com</view>
						</view>
						<view class="address">
							通讯地址:四川省绵阳市电商谷212室
						</view>
					</view>
					<view class="avertar">
						<image src="../../static/contact/avertar.png"></image>
					</view>
				</view>
			</view>
		</view>
		<view class="callphone">
			<button type="primary" @click="call"> 拨打电话 </button>
		</view>
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
				title:"关于我们"
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
		methods:{
			call(){
				uni.makePhoneCall({
					phoneNumber:'13550807080'
				})
			}
		}
	}
</script>

<style lang="scss">
	.contact-container{
		background-color:$uni-bg-color;
		position: relative;
		
		//首页图片
		.banner,image{
			height: 500upx;
			width: 100%;
		}
		
		//团队介绍
		.team{
			display: flex;
			flex-direction: column;
			margin: 20upx;
			margin-top:60upx;
			background-color:$uni-bg-color; 
			border-radius: 20upx;
			padding: 20upx;
			.title{
				text-align: center;
				font-size: $uni-font-size-lg;
				color: #0eb2fe;
				margin: 20upx;
				font-weight: 700;
			}
			
			.desc{
				font-size: $uni-font-size-base;
				color: $uni-text-color;
				text-indent: 2em;
			}
			.pic{
				margin-top:20upx;
			}
			
		}
		
		//价值观
		.values{
			height: 1150upx;
		}
		//联系我们
		.info{
			// display: flex;
			padding: 20upx;
			border-bottom: 1px solid $uni-border-color;
			margin-bottom: 50upx;
			
			
// 			&:nth-last-child(1){
// 				border-bottom: 0;
// 			}
			
			.title{
				margin: 40upx;
				text-align: center;
				font-size: $uni-font-size-lg;
				color: $uni-text-color;
				font-weight: 700;
			}
			.cards{
				background-color: $uni-bg-color;
				border-radius: 20upx;
				padding: 20upx;
				position: relative;
				.card{
					position: relative;
					.info{
						.name{
							font-size: $uni-font-size-lg;
							display: flex;
							font-weight: 700;
							line-height: 35upx;
							align-items: baseline;
							margin-bottom: 20upx;
							.name-desc{
								font-size: $uni-font-size-base;
								color: $uni-text-color-grey;
								margin-left: 14upx;
								line-height: 20upx;
							}
						}
						.phone{
							
							font-size: $uni-font-size-base;
							display: flex;
							margin-bottom: 20upx;

							line-height: 20upx;
							align-items: baseline;
							.phone-desc{
								font-size: $uni-font-size-base;
								color: #0eb2fe;
								margin-left: 14upx;
							}
						}
						.email{
							
							font-size: $uni-font-size-base;
							display: flex;
							margin-bottom: 20upx;
						
							line-height: 20upx;
							align-items: baseline;
							.email-desc{
								font-size: $uni-font-size-base;
								color: #0eb2fe;
								margin-left: 14upx;
							}
						}
						.address{
							font-size: $uni-font-size-sm;
							margin-bottom: 20upx;
							line-height: 20upx;
							color: $uni-text-color-grey;
						}
					}
					.avertar{
						position: absolute;
						width: 150upx;
						height: 150upx;
						right: 35upx;
						top:35upx;
						border: 1px solid #0eb2fe;
						border-radius: 50%;
						
						image{
							width: 130upx;
							height: 130upx;
							vertical-align: middle;
							margin: 10upx;
							
						}
					}
				}
			}
		}
		
		//按钮
		.callphone{
			position: fixed;
			// margin: 10upx;
			padding: 30upx;
			box-sizing: border-box;
			bottom: 0;
			width: 100%;
			// border: 1upx solid red;
			background-color: $uni-bg-color;
			// height: 20upx;
			text-align: center;
		}
	}
</style>
