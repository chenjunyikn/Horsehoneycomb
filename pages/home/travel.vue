<template>
	<view class="travel">
		<!-- 绝对定位广告 -->
		<image src="../../static/travel/530.png" id="fixed" mode=""></image>
		<!-- 轮播图 -->
		<view class="uni-padding-wrap">
			<view class="page-section">
				<view class="page-section-spacing">
					<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration" circular="true">
						<swiper-item class="swiper-one">
							<image src="../../static/travel/qlxlb1.png"  mode="scaleToFill"></image>
						</swiper-item>
						<swiper-item class="swiper-one">
							<image src="../../static/home/lb2.png"  mode="scaleToFill"></image>
						</swiper-item>
						<swiper-item class="swiper-one">
							<image src="../../static/home/lb3.png"  mode="scaleToFill"></image>
						</swiper-item>
					</swiper>
				</view>
			</view>
		</view>
		<!-- 搜索框 -->
		<view class='searchInput999'>
			<view class='searchBox999'>
				<image src='/static/home/icon-search.png' class='search999'></image>
			</view>
			<input class='input999' placeholder="四川" placeholder-style="font-size:15px;"></input>
		</view>
		<!-- icon -->
		<view class="searchInput999-right">
			<uni-icon  type="more-filled" size="30"></uni-icon>
		</view>
		<!-- 九宫格 -->
		<view class="gg">
			<uni-grid class="uni-grid" type="square"  :options='options'  :show-border="false" column-num='5'></uni-grid>
		</view>
		<!-- 三个广告 -->
		<view class="adrate">
			<view class="adrate-left">
				<view class="adrate-left-left">
					<p>领蜂蜜</p>
					<span>蜂蜜抵现金</span>
				</view>
				<view class="adrate-left-right">
					<image src="../../static/travel/lfm.png" mode=""></image>
				</view>
			</view>
			<view class="adrate-center">
				<view class="adrate-center-left">
					<p>高铁游</p>
					<span>周末去哪儿</span>
				</view>
				<view class="adrate-center-right">
					<image src="../../static/travel/lfm.png" mode=""></image>
				</view>
			</view>
			<view class="adrate-right">
				<view class="adrate-right-left">
					<p>高铁游</p>
					<span>周末去哪儿</span>
				</view>
				<view class="adrate-right-right">
					<image src="../../static/travel/lfm.png" mode=""></image>
				</view>
			</view>
		</view>
		<!-- 1元抢爆 -->
		<view class="money">
			<image src="../../static/travel/1y.png" mode=""></image>
		</view>
		<!-- 横向四个广告 -->
		<view class="jq">
			<view class="jq-one"><image src="../../static/travel/jwhc.png" mode=""></image></view>
			<view class="jq-two"><image src="../../static/travel/jnhc.png" mode=""></image></view>
			<view class="jq-three"><image src="../../static/travel/jphcp.png" mode=""></image></view>
			<view class="jq-fore"><image src="../../static/travel/qzhc.png" mode=""></image></view>
		</view>
		<!-- 专属推荐 -->
			<!-- 头部 -->
			<view class="exclusive-top">
				<view class="exclusive-top1">专属推荐</view>
				<view class="exclusive-top2"><image src="../../static/travel/bj.png" mode=""></image></view>
			</view>
			<!-- 横向滑动 -->
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
			  <view class="hr"></view>
			  <!-- 找低价 -->
			  <view class="lowprice">
			  	<view class="low-top">
			  		找低价
			  	</view>
				<view class="low-left">
					<view class="low-left-top">
						每日蜂抢<uni-countdown color="#FFFFFF" background-color="black" border-color="black" :show-day="false" :hour="12" :minute="12" :second="12"></uni-countdown>
					</view>
					<view class="low-left-botton">
						<image src="../../static/travel/mrfq.png" mode=""></image>
						<view class="tglry">泰国六日游</view>
						<view class="mj">
							<view class="mj-left">已满减400元</view>
							<view class="mj-right"> 
								<view class="mj-right-left">￥999</view>
								<view class="mj-right-right">起</view>
							</view>
						</view>
					</view>
				</view>
				<view class="low-right">
					<view class="low-left-top">
						特价机票
					</view>
					<view class="low-right-center">
						<view class="tjjp">许昌出发</view>
						<view class="tj">
							<view class="tj-left">低价出发最划算</view>
							<view class="tj-right">特价</view>
						</view>
						
					</view>
					<view class="low-left-top">
						低价地图
					</view>
					<view class="low-right-center">
						<view class="tjjp">许昌出发</view>
						<view class="tj">
							<view class="tj-left">哪里便宜飞去哪</view>
							<view class="tj-right">特价</view>
						</view>
						
					</view>
				</view>
				
			  </view>
			  <view class="load">
					<uni-load-more status="loading"></uni-load-more>
			  </view>
			  
	</view>
</template>

<script>
	import uniIcon from "@/components/uni-icon/uni-icon.vue"
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	import WucTab from '@/components/wuc-tab/wuc-tab.vue'
	import uniCountdown from "@/components/uni-countdown/uni-countdown.vue"
	import uniLoadMore from "@/components/uni-load-more/uni-load-more.vue"
	export default {
		components: {uniIcon,uniGrid,WucTab,uniCountdown,uniLoadMore},
		data() {
			return {
				options:[
					{image:'../../static/travel/jpcp.png',text:'机票车票'},
					{image:'../../static/travel/gty.png',text:'跟团游'},
					{image:'../../static/travel/zyx.png',text:'自由行'},
					{image:'../../static/travel/dzlx.png',text:'定制旅行'},
					{image:'../../static/travel/yl.png',text:'邮轮'},
					{image:'../../static/travel/ddwl.png',text:'当地玩乐'},
					{image:'../../static/travel/jdmp.png',text:'景点门票'},
					{image:'../../static/travel/jzc.png',text:'机租车'},
					{image:'../../static/travel/qz.png',text:'签证'},
					{image:'../../static/travel/jddj.png',text:'酒店度假'}],
				indicatorDots: false,
				autoplay: true,
				interval: 4000,
				duration: 800,
			}
		},
		onLoad() {

		},
		methods: {}
	}
</script>

<style>
	@import url("../../static/css/travel.css");
</style>
