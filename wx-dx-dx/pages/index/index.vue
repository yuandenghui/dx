<template>
	<view class="content">
		 <view :class="head">
		 	<h1>中国电信营业厅</h1>
		 </view> 
		 <view class="tip">
		 	<span>Hi，welcome！美好的一天从这里开始啦</span>
		 </view>
		 <view class="part_bg one">
			 <view class="one_top">
			 	<span>我的套餐</span>
				<view class="btn">
					关怀版
				</view>
			 </view>	
		 	<view class="one_bottom">
				<view class="item">
					<span class="num">{{tc_arr[0]}}GB</span>
					<span class="ftc224">剩余通用流量</span>
					<span class="btn">流量订购</span>
				</view>
		 		<view class="item">
		 			<span class="num">{{tc_arr[1]}}元</span>
		 			<span class="ftc224">账户余额</span>
		 			<span class="btn">充话费</span>
		 		</view>
				<view class="item">
					<span class="num">{{tc_arr[2]}}分钟</span>
					<span class="ftc224">已用通用语音</span>
					<span class="btn">查语音</span>
				</view>
		 	</view>
		 </view>
		 <view class="part_bg two">
		 	<view class="item">
				<view class="pic_bg">
					<img src="../../static/index/sx.png" alt="">
				</view>
		 		<span class="ft14">套餐用量</span>
		 	</view>
			<view class="item">
				<view class="pic_bg">
					<img src="../../static/index/kd.png" alt="">
				</view>
				<span class="ft14">宽带服务</span>
			</view>
			<view class="item">
				<view class="pic_bg">
					<img src="../../static/index/zd.png" alt="">
				</view>
				<span class="ft14">话费账单</span>
			</view>
			<view class="item">
				<view class="pic_bg">
					<img src="../../static/index/jf.png" alt="">
				</view>
				<span class="ft14">积分兑换</span>
			</view>
		 </view>
		 <view class="part_bg three">
			 <view class="three_top">
			 	<span class="ft18 bold">热门活动</span>
			 	<span class="ft16" style="margin-left: 10px;">超多福利享不停</span>
			 </view>
		 	
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
		 <view class="part_bg four"> 
			 <view class="four_top">
				<span class="ft18 bold">宽带新装</span>
			 </view>
			<view class="four_botttom">
				<view class="">
					<view class="wrap" v-for="(item,index) in four_arr"  >
						<view class="">
							<img :src="item.src" alt="" class="four_img">
						</view>
						<view style="margin: 10px 5px;">{{item.word}}</view>
					</view>
				</view>
				
				<view class="">
					<view class="wrap2" v-for="(item,index) in four_arr2"  >
						<view class="">
							<img :src="item.src" alt="" class="four_img">
						</view>
						<view style="margin: 10px 5px;">{{item.word}}</view>
					</view>
				</view>
				
			</view>
			 
		 </view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				head:'head',
				tc_arr:[66,77,88],
				four_arr:[{src:'../../static/index/kd1.png',word:'9.9元享10GB流量'},
				{src:'../../static/index/kd3.png',word:'数字生活 翼起点亮'},
				{src:'../../static/index/kd5.png',word:'童话改编电影，带你梦回奇幻童年'}
				],
				four_arr2:[{src:'../../static/index/kd2.png',word:'5G终端+5G套餐	'},
				{src:'../../static/index/kd4.png',word:'想与你去看日落美景'} 
				]
			}
		},
		onLoad() {

		},
		onPageScroll(e) {
			 // 动态横幅 动态标题
			if(e.scrollTop>100){
				this.head='head2'
				uni.setNavigationBarTitle({
					title: '电信营业厅',
					success: () => {
						console.log('修改标题成功')
					},
					fail: () => {
						console.log('修改标题失败')
					},
					complete: () => {
						console.log('修改标题结束')
					},
				})
 
			}else{
				this.head='head'
				uni.setNavigationBarTitle({
					title: '',
					success: () => {
						console.log('修改标题成功')
					},
					fail: () => {
						console.log('修改标题失败')
					},
					complete: () => {
						console.log('修改标题结束')
					},
				})
			}
     	},

		methods: {

		}
	}
</script>

<style>
	 
	.ftc224{
		color: #ccc;
	}
	.ft14{
		font-size: 14px;
	}
	.ft16{
		font-size: 16	px;
	}
	.ft18{
		font-size: 18px;
	}
	.bold{
		font-weight: bold;
	}
	.content {  
		overflow: hidden;
		position: relative; 
		padding-bottom: 20px; 
		height: 100%;
		background: url('../../static/bgd/bg.jpg.jpg');
		background-size: 100% 150%;
	}
	.head { 
		padding: 30px 20px 20px 20px;
	    position: fixed; 
		font-size: 16rpx;
		color: white; 
		width: 100%;
		height: 20px;
	}
	.head2 {
		padding: 30px 20px 20px 20px;
	    position: fixed; 
		font-size: 16rpx;
		color: black;
		background-color: rgb(192, 222, 249);
		width: 100%;
		height: 20px;
	}
	.tip{
		margin:0rpx 20rpx;
		 margin-top: 100px;
		padding: 20rpx 20rpx;
		background: rgb(229, 239, 248);
		font-size: 10rpx;
	}
	.part_bg{
		background: rgb(255, 255, 255);
	}
	.one{
		margin:0rpx 20rpx;
		margin-top: 20px;
		/* height: 500rpx; */
		border-radius: 6px;
		padding: 20px 10px 40px 10px;
	}
	.one .one_top{
		display: flex;
		justify-content: space-between; 
	}
	.one .one_top .btn{
		 padding: 4px 8px;
		 border: 2px solid rgb(250, 216, 163);
		 color: rgb(250, 216, 163);
		 border-radius: 10px;
		 font-size: 10px;
	}
	.one .one_bottom{ 
		 margin-top: 20px;
		 display: flex;
		 justify-content: space-between;	
		 font-size: 14px;
	}
	.one .one_bottom .item{
		 display: flex;
		 flex-direction: column;
	}
	.one .one_bottom .btn{
		padding: 4px 0px;
		text-align: center;
		background: rgb(224, 239, 253);
		color: rgb(76, 169, 254);
		border-radius: 12px;
	}
	.one .one_bottom .item span{
		 margin-top: 4px;
	}
	.one .one_bottom .item .num{
		text-align: center;
	}
	.two{
		padding: 30px 30px 10px 30px;
		display: flex;
		 justify-content: space-between;
		margin:0rpx 20rpx;
		margin-top: 20px; 
	}
	 .two .item{
		 display: flex;
		 flex-direction: column;
		text-align: center;	
	 }
	 .two .item .pic_bg{ 
		 padding: 12px 0px 10px 0px;
		 border-radius: 50%;
	 	 background: rgb(234, 244, 254);
		 margin-bottom: 10px;
	 }
	.three{
		margin:0rpx 20rpx;
		margin-top: 20px; 
		border-radius: 6px;
		padding: 20px 10px 40px 10px;
	}
	.three .three_bottom{
		margin-top: 20px;
		display: flex;
		justify-content: space-between;
	}
	.three .three_bottom .item{
		padding: 10px 10px;
		border: 1px solid  #ccc;
		border-radius: 6px;
		box-shadow:  0 0 5px red ;
	}
	.three .three_bottom .item .pic{
		margin-top: 10px;
		width: 150px;
		height: 130px;
	}
	.four{
		margin:0rpx 20rpx;
		margin-top: 20px;  
		border-radius: 6px;
		padding: 20px 10px 40px 10px;
		background: rgb(245, 245, 245);
	}
	.four .four_botttom{
		display: flex; 
		 
	}
	
	.four .four_botttom .wrap{ 
		overflow: hidden;
		border-radius: 14px;
		background: #fff;
		margin: 10px 10px;
		padding-bottom:20px ;
		width: 160px;
		 
	}
	.four .four_botttom .wrap2{
		overflow: hidden;
		border-radius: 14px;
		background: #fff;
		margin: 10px 10px;
		padding-bottom:20px ;
		width: 160px;
		 
	}
	.four .four_botttom .four_img{ 
		width: 160px;
		height: 100%;
	}
</style>
