<template>
	<view class="const">
		<!-- 绝对定位加号 -->
		<view class="jh">
			+
		</view>
		<view class="top">
			<!-- 轮播图 -->
			 <view class="uni-padding-wrap">
				<view class="page-section">
					<view class="page-section-spacing">
						<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration" circular="true">
							<swiper-item class="swiper-one">
								<image src="../../static/home/lb1.png"  mode="scaleToFill"></image>
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
				<input class='input999' placeholder="三亚" placeholder-style="font-size:15px;"></input>
			</view>
			<view class="right">
				<uni-icon  type="chat" size="22"></uni-icon>
			</view>
			<!-- 九宫格 -->
			<view class="gg">
				<uni-grid class="uni-grid" type="square"  :options='options'  :show-border="false" column-num='5'></uni-grid>
			</view>
			<!-- 横向选项卡 -->
		    <view class="wuctab">
				  <wuc-tab :tab-list="tabList" :tabCur.sync="TabCur"  selectClass="text" @change="tabChange"></wuc-tab>
					<swiper :current="TabCur" duration="300" class="swiper"  @change="swiperChange">
						  <swiper-item class="swiper-item"  v-for="(item,index) in tabList"  :key="index" >
									<view v-show="TabCur === 0">
										<travel></travel>
									</view>
									<view v-show="TabCur === 1">
										<recommend></recommend>
									</view>
									<view v-show="TabCur === 2">
										<video></video>
									</view>
									<view v-show="TabCur === 3">
										<inland></inland>
									</view>
									<view v-show="TabCur === 4">
										<foreign></foreign>
									</view>
									<view v-show="TabCur === 5">
										<boy></boy>
									</view>
									<view v-show="TabCur === 6">
										<island></island>
									</view>
									<view v-show="TabCur === 7">
										<lovers></lovers>
									</view>
									<view v-show="TabCur === 8">
										<selfs></selfs>
									</view>
						  </swiper-item>
					</swiper>
			</view>
			
		</view>
	</view>
</template>

<script>
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	import uniIcon from "@/components/uni-icon/uni-icon.vue"
	import WucTab from '@/components/wuc-tab/wuc-tab.vue'
	import travel from '../pager/travel.vue'
	import recommend from '../pager/recommend.vue'
	import video from '../pager/video.vue'
	import inland from '../pager/inland.vue'
	import foreign from '../pager/foreign.vue'
	import boy from '../pager/boy.vue'
	import lovers from '../pager/lovers.vue'
	import selfs from '../pager/selfs.vue'
	import island from '../pager/island.vue'
	export default {
		components:{
			uniGrid,
			uniIcon,
			WucTab,
			travel,
			recommend,
			video,
			inland,
			foreign,
			boy,
			lovers,
			selfs,
			island
		},
		data() {
			return {
				TabCur: 0,
				indicatorDots: false,
				autoplay: true,
				interval: 4000,
				duration: 800,
				options:[
					{image:'../../static/home/gl.png',text:'攻略'},
					{image:'../../static/home/djd.png',text:'订酒店'},
					{image:'../../static/home/jphcp.png',text:'机票车票'},
					{image:'../../static/home/qlx.png',text:'去旅行'},
					{image:'../../static/home/yj.png',text:'游记'}],
					 tabList: [
						{ name: '正在旅行' },
						{ name: '推荐' },
						{ name: '视频' },
						{ name: '国内' },
						{ name: '国外' },
						{ name: '带娃旅行' },
						{ name: '海岛游' },
						{ name: '情侣出行'},
						{ name: '自驾游'}
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
			}
		}
		}	
</script>

<style>
	@import url("../../static/css/home.css");
	/* @import "~@/styles/icon.scss"; */
</style>
