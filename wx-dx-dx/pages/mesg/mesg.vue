<template>
	<view class="content">
		 <view class="wrap">
		 	<view class="line"> 
		 	</view>
			<view class="item">
				<view class="top">
					<span>话费省钱小助手</span>
					<span>></span>
				</view>
				<view class="bottom">
					不知道选什么套餐？试试这个	
				</view>
			</view>
		 </view>
		 
		 <view class="wrap">
		 	<view class="line"> 
		 	</view>
		 			<view class="item">
		 				<view class="top">
		 					<span>流量不够？加个救急包，很优惠！</span>
		 					<span class="point_wrap">
								<view class="point"></view>
								></span>
		 				</view>
		 				<view class="bottom">
		 					还有假日包，深夜包等候您选	
		 				</view>
		 			</view>
		 </view>
		 
		 <view class="wrap">
		 	<view class="line"> 
		 	</view>
		 			<view class="item">
		 				<view class="top">
		 					<span>爱心翼站，温暖在您身边!</span>
		 					<span>></span>
		 				</view>
		 				<view class="bottom">
		 					查找距离您最近的 "爱心翼站"	
		 				</view>
		 			</view>
		 </view>
		 
		 <view class="end">
		 	<span>—— 到底啦 ——</span>
		 </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'mesg'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	uni-page-body, uni-page-refres {
	    display: block;
	    box-sizing: border-box;
	    width: 100%;
	    height: 100% !important;
	}
	.content {
		 background: rgb(250, 250, 250);
		 padding: 0px 20px;
		 height: 100%; 
	}
	.wrap{
		padding-top: 10px;
	}
	.wrap .item{
		background: #fff;
		margin-top: 10px;
		border-radius: 8px;
		padding: 18px 10px;
		font-size: 14px;
	}
	.wrap .item .top{
		display: flex;
		justify-content: space-between;
		border-bottom: 1px solid #ccc;
		padding-bottom: 10px;
	}
	.wrap .item .top .point{
		width: 4px;
		height: 4px;
		border-radius: 1px;
		background: red;
		margin-right: 6px;
		}
    .wrap .item .top .point_wrap{
		display: flex;
		align-items: center;
	}
	.wrap .item .bottom{
		margin-top: 4px;
		color: #ccc;
	}
	.line{ 
		position: relative; 
	}
	.line::after{ 
		content: '';
		position: absolute; 
		bottom: 0; 
		height: 3px; 
		width: 20px; 
		background-color: #ccc; 
		left: 50%; 
		transform: translateX(-50%);
	}
	.end{
		width: 100%;
		text-align: center;
		margin-top: 20px;
		color: #ccc;
		font-size: 14px;
	}
</style>
