<template>
	<view class="content">
		<view class="tab">
			<view :class="this.tab==='0'?'act':''" @click="tabchange('0')">话费</view>
			<view :class="this.tab==='1'?'act':''" @click="tabchange('1')">套餐</view>
			<view :class="this.tab==='2'?'act':''" @click="tabchange('2')">流量</view>
		</view>
		  
		  
		  
		  <view class="part_one">
			 <view class="">
			 	<span>话费</span>
			 </view>
			 <view class="wrap">
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
			 	 
			 </view>
		  	
		  </view>
		  
		 <view class="part_one">
		 			 <view class="">
		 			 	<span>套餐</span>
		 			 </view>
		 			 <view class="wrap">
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
		 			 	 
		 			 	 
		 			 </view>
		 	
		 </view>
		  
		  <view class="part_one">
		  			 <view class="">
		  			 	<span>流量</span>
		  			 </view>
		  			 <view class="wrap">
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
		  			 	 
		  			 </view>
		  	
		  </view>
		  
		   
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'yewu',
				tab:'0'
			}
		},
		onLoad() {

		},
		methods: {
		tabchange(n){
			this.tab=n
		}
		}
	}
</script>

<style >
	  uni-page-body, uni-page-refres {
	    display: block;
	    box-sizing: border-box;
	    width: 100%;
	    height: 100% !important;
	}
	.ft14{
		font-size: 14px;
	}
	.content {
		 background: rgb(250, 250, 250);
		 padding: 0px 20px;
		 height: 100%; 
	}
	.content .tab{
		display: flex;
		justify-content: space-between;
		padding: 30px;
	}
	.act{ 
		color: rgb(31, 147, 254);
		font-size: 18px;
		padding-bottom: 4px;
		position: relative;
	}
	.act:after{ 
	 content: ''; 
	 position: absolute; 
	 bottom: 0; 
	 height: 1px; 
	 width: 20px; 
	 background-color: rgb(31, 147, 254); 
	 left: 50%; 
	 transform: translateX(-50%);
	}
	.part_one{
		background: white; 
		border-radius: 6px; 
		padding: 10px 10px 10px 10px;
		display: flex; 
		flex-direction: column;
		margin-bottom: 20px; 
	}
	.part_one .wrap{ 
		padding: 10px 10px 10px 10px;
		display: flex;  
	}
	.part_one .item{
			display: flex;
			flex-direction: column;
			text-align: center;	
			margin: 10px 20px 10px 20px;
	}
	.part_one .item .pic_bg{ 
			 padding: 12px 0px 10px 0px;
			 border-radius: 50%;
		     background: rgb(234, 244, 254);
			 margin-bottom: 10px;
	}
</style>
