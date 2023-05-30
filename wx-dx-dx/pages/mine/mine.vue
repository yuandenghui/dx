<template>
	<view class="content">
	 <view class="head">
		 <view class="item">
		 	<img class="img" src="../../static/index/my4.png" alt="">
		 </view>
		<view class="item2">
			<view class="item">
				<img src="../../static/index/my6.png" alt="">
						<span>切换</span>
			</view>
			<view class="item">
				<img src="../../static/index/my5.png" alt="">
						<span>设置</span>
			</view>
		</view>
		  
	 </view>
	 <view class="bgfff two padding">
		 <view class="item">
			 <span>--GB</span>
		 	<span>剩余通用流量</span>
		 </view>
		 <view class="item">
			 <span>--元</span>
		 	<span>账户余额</span>
		 </view>
		 <view class="">
		 	<img src="../../static/index/my1.png" alt="">
		 </view>
	 </view>
	 <view class="bgfff box">
		 <view class="three"> 
			<view class="three_bottom">
				<view class="item">
					<span>特惠流量</span>
					<view >
						<img class="pic" src="../../static/index/dy.png" alt="">
					</view>
				</view>
				<view class="item">
					<span>流量暖心包</span>
					<view >
						<img class="pic" src="../../static/index/nx.png" alt="">
					</view>
				</view>
			</view>
		 </view>
	 </view>
	  
	 <view class="bgfff box four padding">
		 <view class="">
		 	<span>服务办理</span>
		 	<span class="text2">便捷服务更快一步</span>
		 </view>
	 		<view class="box2">
				<view class="item">
					<img src="../../static/index/my3.png" alt="">
					<span>订单查询</span>
				</view>
				<view class="item">
					<img src="../../static/index/my3.png" alt="">
					<span>订单查询</span>
				</view>
				<view class="item">
					<img src="../../static/index/my3.png" alt="">
					<span>订单查询</span>
				</view>
				<view class="item">
					<img src="../../static/index/my3.png" alt="">
					<span>订单查询</span>
				</view>
				<view class="item">
					<img src="../../static/index/my3.png" alt="">
					<span>订单查询</span>
				</view>
				<view class="item">
					<img src="../../static/index/my3.png" alt="">
					<span>订单查询</span>
				</view>
				<view class="item">
					<img src="../../static/index/my3.png" alt="">
					<span>订单查询</span>
				</view>
				<view class="item">
					<img src="../../static/index/my3.png" alt="">
					<span>订单查询</span>
				</view>
	 		</view>
	 </view>
	 <view class="bgfff box padding">
	 	<img src="../../static/index/my2.png" alt="">
	 </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'mine'
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
	     
	}
	.colorc{
		color: #ccc;
	}
	.padding{
		margin: 0px 20px;
	}
	.content { 
		 height: 100%;
		 background: rgb(250, 250, 250); 
	}
	.head{
		padding: 10px 20px 10px 10px;
		display: flex;
		justify-content: space-between;
		background: #d4e1ec;
		background-image: linear-gradient(#d4e1ec, #fff)
	}
	.head .item{
		display: flex;
		flex-direction: column;
	}
	.head .item .img{
		width: 60px;
		margin-left: 20px;
	}
	.head .item2{
		display: flex; 
		 
	}
	.head .item2 .item{
		display: flex;
		flex-direction: column;
		margin-left: 30px;
	}
	.two{ 
		display: flex;
		justify-content: space-between;
		padding: 20px 10px;
	}
	.two .item{
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	 
	.text2{
		margin-left: 10px;
		font-size: 12px;
		color: #ccc;
	}
	.bgfff{
		background: #fff;
	}
	.head{
		height: 100px;
	}
	.box{
		width: 100%;
		 
		margin-top:10px;
	}
	.box .box2{
		display: flex;
		flex-wrap: wrap;
	}
	.box .box2 .item{
		font-size: 12px;
		width: 80px;
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 10px 10px 0px 0px;
	}
	.box2 img{
		width: 40px;
	}
	.three{
		margin:0rpx 20rpx;
		margin-top: 20px; 
		border-radius: 6px;
		padding: 20px 10px 40px 10px;
	}
	.three .three_bottom{ 
		display: flex;
		justify-content: space-between;
	}
	 
	.three .three_bottom .item .pic{
		margin-top: 10px;
		width: 150px;
		height: 100px;
	}
	.four{
		padding: 20px 10px 30px 10px;
	}
</style>
