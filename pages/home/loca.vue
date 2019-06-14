<template>
	<view class="loca">
		<view class="ptop">
			<!-- <image src="../../static/top.png" mode=""></image> -->
			<view class="zk">
				周口<uni-icon  type="arrowdown" color="white" size="22"></uni-icon>
			</view>
			<view class='searchInput999'>
				<view class='searchBox999'>
					<image src='/static/home/icon-search.png' class='search999'></image>
				</view>
				<input class='input999' placeholder="搜索当地玩乐/美食/路线等" placeholder-style="font-size:15px;"></input>
			</view>
		</view>
		<!-- 九宫格 -->
		<view class="grid">
			<uni-grid class="uni-grid" type="square"  :options='options'  :show-border="false" column-num='5'></uni-grid>
		</view>
		<!-- 横向选择卡 -->
		<view class="wuctab">
			  <wuc-tab :tab-list="tabList" :tabCur.sync="TabCur"  selectClass="text" @change="tabChange"></wuc-tab>
				<swiper :current="TabCur" duration="300" class="swiper"  @change="swiperChange">
					  <swiper-item class="swiper-item"  v-for="(item,index) in tabList"  :key="index" >
								<view v-show="TabCur === 0">
									<play></play>
								</view>
								<view v-show="TabCur === 1">
									aa
								</view>
								<view v-show="TabCur === 2">
									vv
								</view>
					  </swiper-item>
				</swiper>
		</view>
		<view class="hr"></view>
		<!-- 住哪里 -->
		<view class="home">
			<view class="znl">
				<text>住哪里</text>
			</view>
			<!-- scroll-view横向滑动  -->
			<view class="scroll_box"> 
				<scroll-view class="scroll-view_x" scroll-x style="width: auto;overflow:hidden;">
				  <view class="item_a" >
						<image src="../../static/loca/hy.png" class="item_book_img" mode="aspectFill"></image>
				  </view>
				  <view class="item_b" >
				  		<image src="../../static/loca/sj.png" class="item_book_img1" mode="aspectFill"></image>
				  </view>
				  <view class="item_c">
				  		<image src="../../static/loca/mp.png" class="item_book_img2" mode="aspectFill"></image>
				  </view>
				  <view class="item_d">
				 		<image src="../../static/loca/ht.png" class="item_book_img3" mode="aspectFill"></image>
				  </view>
				  <view class="item_e">
				  		<image src="../../static/loca/xtd.png" class="item_book_img4" mode="aspectFill"></image>
				  </view>
				</scroll-view>
			  </view>
		</view>
		<view class="hr">
			
		</view>
		<!-- 旅行商城 -->
		<view class="shopping">
			<view class="znl">
				<text>旅行商城</text>
			</view>
			<view class="shopp-one">
				<image src="../../static/loca/tqg.png" class="shopp-one_img" mode="aspectFill"></image>
			</view>
			<view class="shopp-two">
				<image src="../../static/loca/mdg.png" class="shopp-two_img" mode="aspectFill"></image>
			</view>
			<view class="shopp-three">
				<image src="../../static/loca/fxl.png" class="shopp-three_img" mode="aspectFill"></image>
			</view>
		</view>
		<view class="hr"></view>
		<!-- 热门游记 -->
		<view class="notes">
			<view class="znl">
				<text>热门游记</text>
				<text class="chakan">查看更多 ></text>
			</view>
			<!-- scroll-view横向滑动  -->
			<view class="scroll_notes"> 
				<scroll-view class="scroll-view_x" scroll-x style="width: auto;overflow:hidden;">
				  <view class="notes_a" >
						<image src="../../static/loca/zkx.png" class="notes_book_img" mode="aspectFill"></image>
				  </view>
				  <view class="notes_b" >
				  		<image src="../../static/loca/bh.png" class="notes_book_img1" mode="aspectFill"></image>
				  </view>
				  <view class="notes_c">
				  		<image src="../../static/loca/nns.png" class="notes_book_img2" mode="aspectFill"></image>
				  </view>
				  <view class="notes_d">
				 		<image src="../../static/loca/jy.png" class="notes_book_img3" mode="aspectFill"></image>
				  </view>
				  <view class="notes_e">
				  		<image src="../../static/loca/lzhl.png" class="notes_book_img4" mode="aspectFill"></image>
				  </view>
				</scroll-view>
			  </view>
		</view>
		<view class="hr"></view>
		<!-- 周边目的地 -->
		<view class="circum">
			<view class="znl">
				<text>周边目的地</text>
			</view>
			<view class="circum-one">
				<image src="../../static/loca/lhs.png" mode=""></image>
			</view>
			<view class="circum-two">
				<image src="../../static/loca/zmd.png" mode=""></image>
			</view>
			<view class="circum-three">
				<image src="../../static/loca/xc.png" mode=""></image>
			</view>
		</view>
		<!-- 查看更多 -->
		<view class="map">
			地图上查看地图 >
		</view>
	</view>
</template>

<script>
	import uniIcon from "@/components/uni-icon/uni-icon.vue"
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	import WucTab from '@/components/wuc-tab/wuc-tab.vue'
	import play from '../locatn/play.vue'
	export default {
		components:{
			uniGrid,
			uniIcon,
			WucTab,
			play
		},
		data() {
			return {
					 scrollTop: 0,
					 old: {
						scrollTop: 0
					},
					TabCur: 0,
					options:[
					{image:'../../static/loca/jdwl.png',text:'景点玩乐'},
					{image:'../../static/home/djd.png',text:'订酒店'},
					{image:'../../static/loca/ms.png',text:'美食'},
					{image:'../../static/home/qlx.png',text:'当地游'},
					{image:'../../static/loca/wd.png',text:'问答'}],
					tabList: [
						{ name: '怎么玩' },
						{ name: '吃什么' },
						{ name: '买什么' }
					]
			}
		},
		onLoad() {

		},
		methods: { 
			tabChange(index) {
				this.TabCur = index;
			},
			  swiperChange(e) {
				let { current } = e.target;
				this.TabCur= current;
			},
			 scroll: function(e) {
				console.log(e)
				this.old.scrollTop = e.detail.scrollTop
			}
		}
	}
</script>

<style>
	@import url("../../static/css/loca.css");
</style>
