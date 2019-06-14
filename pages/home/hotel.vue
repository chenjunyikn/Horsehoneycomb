<template>
	<view class="home">
		<!-- 轮播图 top-0 -->
		<view class="uni-padding-wrap">
			<view class="page-section">
				<view class="page-section-spacing">
					<swiper class="swiper" indicator-active-color="yellow" indicator-color="white" :indicator-dots="indicatorDots" indicator-dots="true" :autoplay="autoplay" :interval="interval" :duration="duration" circular="true">
						<swiper-item class="swiper-one">
							<image src="../../static/hotel/lb3.png"  mode="scaleToFill"></image>
						</swiper-item>
						<swiper-item class="swiper-one">
							<image src="../../static/hotel/lb2.png"  mode="scaleToFill"></image>
						</swiper-item>
						<swiper-item class="swiper-one">
							<image src="../../static/hotel/lb1.png"  mode="scaleToFill"></image>
						</swiper-item>
					</swiper>
				</view>
			</view>
		</view>
		<!-- 横向五个广告 -->
		<view class="guanggao">
			<view class="guanggao-one"><image src="../../static/hotel/gg1.png" mode=""></image></view>
			<view class="guanggao-two"><image src="../../static/hotel/gg2.png" mode=""></image></view>
			<view class="guanggao-three"><image src="../../static/hotel/gg3.png" mode=""></image></view>
			<view class="guanggao-fore"><image src="../../static/hotel/gg4.png" mode=""></image></image></view>
			<view class="guanggao-five"><image src="../../static/hotel/gg5.png" mode=""></image></view>
		</view>
		<!-- 超值特惠 -->
		<view class="shoppings">
			<view class="shoppings-one">热门精选</view>
			<view class="shoppings-two">
				<view class="shoppings-two-left"><image src="../../static/hotel/500.png" mode=""></image></view>
				<view class="shoppings-two-center">呼伦贝尔咋住</view>
				<view class="shoppings-two-right">泸沽湖异构生活</view>
			</view>
			<!-- scroll-view横向滑动  -->
			<view class="scroll_box"> 
				<scroll-view class="scroll-view_x" scroll-x style="width: auto;overflow:hidden;">
				  <view class="item_a" >
						<image src="../../static/travel/xccf.png" class="item_book_img" mode="aspectFill"></image>
				  </view>
				  <view class="item_b" >
				  		<image src="../../static/travel/jq.png" class="item_book_img1" mode="aspectFill"></image>
				  </view>
				  <view class="item_c">
				  		<image src="../../static/travel/yry.png" class="item_book_img2" mode="aspectFill"></image>
				  </view>
				  <view class="item_d">
				 		<image src="../../static/travel/zyxdz.png" class="item_book_img3" mode="aspectFill"></image>
				  </view>
				  <view class="item_e">
				  		<image src="../../static/travel/ckgd.png" class="item_book_img4" mode="aspectFill"></image>
				  </view>
				</scroll-view>
			  </view>
		</view>
		<!-- 曼谷怎么玩 -->
		<view class="mgplay">
			
		</view>
	</view>
</template>

<script>
	import uniSegmentedControl from "@/components/uni-segmented-control/uni-segmented-control.vue"
	export default {
		components: {uniSegmentedControl},
		data() {
			return {
				 current: 0,
				 // 轮播图
				 indicatorDots: false,
				 autoplay: true,
				 interval: 4000,
				 duration: 800
			}
		},
		onLoad() {

		},
		methods: {
				onClickItem(index) {
							if (this.current !== index) {
								this.current = index;
					}
				}
			}
		}
</script>

<style>
	@import url("../../static/css/hotel.css");
</style>
