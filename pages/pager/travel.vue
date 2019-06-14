<template>
	<view class="content">
		<!-- scroll-view横向滑动  -->
		<view class="scroll_box"> 
			<scroll-view class="scroll-view_x" scroll-x style="width: auto;overflow:hidden;">
			  <view class="item_a" >
					<image src="../../static/home/rmwf.png" class="item_book_img" mode="aspectFill"></image>
			  </view>
			  <view class="item_b" >
			  		<image src="../../static/home/lyqn.png" class="item_book_img1" mode="aspectFill"></image>
			  </view>
			  <view class="item_c">
			  		<image src="../../static/home/zj.png" class="item_book_img2" mode="aspectFill"></image>
			  </view>
			  <view class="item_d">
			 		<image src="../../static/home/dw.png" class="item_book_img3" mode="aspectFill"></image>
			  </view>
			  <view class="item_d">
			  			 		
			  </view>
			</scroll-view>
		  </view>
		  <!-- 旅游景点列表 -->
		  <view class="Scenic">
			  <!-- 左半部分 -->
		  	 <view class="Scenic-left">
				  <view class="Scenic-left-one">
					  <image src="../../static/home/l1.png" mode=""></image>
				  </view>
				  <view class="Scenic-left-two">
					  <image src="../../static/home/l2.png" mode=""></image>
				  </view>
				 <view class="Scenic-left-three">
				  		<image src="../../static/home/l3.png" mode=""></image>
				  </view>
			 </view>
			 <!-- 右半部份 -->
		  	 <view class="Scenic-rigth">
				 <view class="Scenic-rigth-one">
				 		<image src="../../static/home/r1.png" mode=""></image>	  
				 </view>
				 <view class="Scenic-rigth-two">
				 		<image src="../../static/home/r2.png" mode=""></image>	  
				 </view>
				 <view class="Scenic-rigth-three">
				 		<image src="../../static/home/r3.png" mode=""></image>	  
				 </view>
			 </view>
			 <!-- 我是有底线的 -->			 
		  </view>
		  <view class="Scenic-bottom">
			<uni-load-more status="loading"></uni-load-more>
		  </view>
	</view>
</template>

<script>
	import uniLoadMore from "@/components/uni-load-more/uni-load-more.vue"
	export default {
		components: {uniLoadMore},
		data() {
			return {
				 scrollTop: 0,
				 old: {
					scrollTop: 0
				}
			}
		},
		onLoad() {

		},
		methods: {
			 scroll: function(e) {
				console.log(e)
				this.old.scrollTop = e.detail.scrollTop
			}
		}
	}
</script>

<style>
	.content {
		text-align: center;
		height: 400upx;
	}

	.logo {
		height: 200upx;
		width: 200upx;
		margin-top: 200upx;
	}

	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
</style>
