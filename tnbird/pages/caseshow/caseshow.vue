<template>
	<view class="caseshow-container">
		<view class="content">
			<view class="item">
				<view class="pic">
					
					<scroll-view scroll-y>
						<view><image src="../../static/example/16.png" mode="widthFix"></image></view>
					</scroll-view>
				</view>
				<view class="name">XXX小程序模板一</view>
				<view class="tags">
					<view class="tag-item" >电商</view>
					<view class="tag-item" >支付</view>
					<view class="tag-item" >企业独家</view>
					<view class="tag-item" >功能定制</view>	
				</view>
				<view class="desc">
					小程序的简要介绍一
					小程序的简要介绍一
				</view>
			</view>
			<view class="item">
				<view class="pic">
					
					<scroll-view scroll-y>
						<view><image src="../../static/example/16.png" mode="widthFix"></image></view>
					</scroll-view>
				</view>
				<view class="name">XXX小程序模板二</view>
				<view class="tags">
					<view class="tag-item" >电商</view>
					<view class="tag-item" >支付</view>	
				</view>
				<view class="desc">
					小程序的简要介绍二
				</view>
			</view>
			<view class="item">
				<view class="pic">
					
					<scroll-view scroll-y>
						<view><image src="../../static/example/16.png" mode="widthFix"></image></view>
					</scroll-view>
				</view>
				<view class="name">XXX小程序模板三</view>
				<view class="tags">
					<view class="tag-item" >电商</view>
					<view class="tag-item" >支付</view>
					<view class="tag-item" >企业独家</view>
					<view class="tag-item" >功能定制</view>
						<view class="tag-item" >呵呵哒</view>	

					<view class="tag-item" >不错哦</view>	
					<view class="tag-item" >很厉害嘛</view>	

				</view>
				<view class="desc">
					小程序的简要介绍三
					小程序的简要介绍三
					小程序的简要介绍三
				</view>
			</view>
			<view class="item">
				<view class="pic">
					
					<scroll-view scroll-y>
						<view><image src="../../static/example/16.png" mode="widthFix"></image></view>
					</scroll-view>
				</view>
				<view class="name">XXX小程序模板四</view>
				<view class="tags">
					<view class="tag-item" >电商</view>
				</view>
				<view class="desc">
					
					小程序的简要介绍三
					小程序的简要介绍四
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
				border: 1upx solid purple;
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
					color: $uni-text-color;
				}
				
				.tags{
					display: flex;
					flex-wrap: wrap;
					justify-content: space-between;
					
					.tag-item{
						// margin-top:10upx;
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
						margin-top: 10upx;
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
