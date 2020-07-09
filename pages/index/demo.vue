<template>
	<view>
		<view class="example-body">
			<uni-nav-bar :fixed="false" color="#424134" background-color="#FFFFFF" right-icon="scan" @clickLeft="showCity"
			 @clickRight="scan">
				<block slot="left">
					<view class="city">
						<view></view>
						<uni-icons type="location" color="#000000" size="22" />
					</view>
				</block>
				<view class="nav-bar-input">
					<uni-icons class="input-uni-icon" type="search" size="25" color="#000000" />
					<input confirm-type="search" class="nav-bar-input" type="text" style="padding-left: 30px;" placeholder="车厘子"
					 @confirm="confirm">
				</view>
			</uni-nav-bar>
		</view>
		<view class="content">
			<image src="../../static/gua.png"></image>
		</view>
		<view class="sp_text">
			<view class="square">
				<view class="text">
					<h5>专题预售</h5>
					<p>带来偏远地区的原生鲜果送去一份份温暖的爱心</p>
				</view>
			</view>
			<view class="square2">
				<view class="text">
					<h5>邀请好友</h5>
					<p>30元红包等你享</p>
				</view>
			</view>
			<view class="square3">
				<view class="text">
					<h5>扶贫助困</h5>
					<p>带来自然鲜果送去温暖爱心</p>
				</view>
			</view>
		</view>
		<view class="font_sile">
			<span>鲜果快报</span>
			<uni-notice-bar showIcon="true" scrollable="true" single="true" text="今年的砂糖橘,为何这般甜!"></uni-notice-bar>
		</view>
		<view class="Spell">
			<p><span id="sp">拼团预售</span><span>产地直采·品质保证</span></p>
		</view>
		<view class="goods_slie">
			<view class="content">
				<space-swiper></space-swiper>
			</view>
		</view>
		<view class="Spell">
			<p><span id="sp">热卖优惠</span><span>人气销售·大众喜欢</span></p>
		</view>
		<view class="goods_list">
			<view>
				<view class="row">
					<view class="col">
						<image src="../../static/bingtangcheng.jpg"></image>
						<p class="c_title">广西四会砂糖橘</p>
						<p class="c_price"><span>￥26.0</span>/份<cmd-icon class="c_icon" type="add-circle" size="20" color="#fe0000"></cmd-icon>
						</p>
					</view>
					<view class="col">
						<image src="../../static/chelizi.jpg"></image>
						<p class="c_title">智利车厘子</p>
						<p class="c_price"><span>￥69.0</span>/份<cmd-icon class="c_icon" type="add-circle" size="20" color="#fe0000"></cmd-icon>
						</p>
					</view>
					<view class="col">
						<image src="../../static/shengnvguo.jpg"></image>
						<p class="c_title">海南圣女果</p>
						<p class="c_price"><span>￥25.0</span>/份<cmd-icon class="c_icon" type="add-circle" size="20" color="#fe0000"></cmd-icon>
						</p>
					</view>
					<view class="col">
						<image src="../../static/bingtangcheng.jpg"></image>
						<p class="c_title">广西四会砂糖橘</p>
						<p class="c_price"><span>￥26.0</span>/份<cmd-icon class="c_icon" type="add-circle" size="20" color="#fe0000"></cmd-icon>
						</p>
					</view>
					<view class="col">
						<image src="../../static/chelizi.jpg"></image>
						<p class="c_title">智利车厘子</p>
						<p class="c_price"><span>￥69.0</span>/份<cmd-icon class="c_icon" type="add-circle" size="20" color="#fe0000"></cmd-icon>
						</p>
					</view>
					<view class="col">
						<image src="../../static/shengnvguo.jpg"></image>
						<p class="c_title">海南圣女果</p>
						<p class="c_price"><span>￥25.0</span>/份<cmd-icon class="c_icon" type="add-circle" size="20" color="#fe0000"></cmd-icon>
						</p>
					</view>
				</view>
			</view>
		</view>
		<view class="shangxin">
			<view class="Spell">
				<p><span id="sp">时令上新</span><span>应急鲜果·优质果园</span></p>
			</view>
			<view class="uni-flex uni-column">
				<view class="flex-item flex-item-V uni-bg-red">
					<view class="flex_img">
						<image src="../../static/taoxingli.jpg"></image>
					</view>
					<view class="flex_text">
						<span class="f_t_title">广西水蜜桃*5个 约500g</span>
						<p>果肉细腻，酸甜可口，果香沁人</p>
						<p>采摘日期：06.16</p>
						<p>
							<span class="flex_text_p">￥25.0</span>/份
							<cmd-icon class="text_icon" type="add-circle" size="20" color="#fe0000"></cmd-icon>
						</p>
					</view>
				</view>
				<view class="flex-item flex-item-V uni-bg-green">
					<view class="flex_img">
						<image src="../../static/pingguo.jpg"></image>
					</view>
					<view class="flex_text">
						<span class="f_t_title">法国嘎啦苹果*6 约800g</span>
						<p>果肉细腻，酸甜可口，果香沁人</p>
						<p>采摘日期：06.16</p>
						<p>
							<span class="flex_text_p">￥25.0</span>/份
							<cmd-icon class="text_icon" type="add-circle" size="20" color="#fe0000"></cmd-icon>
						</p>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import uniNavBar from "@/components/uni-nav-bar/uni-nav-bar.vue"
	import uniIcons from "@/components/uni-icons/uni-icons.vue"
	import uniNoticeBar from '@/components/uni-notice-bar/uni-notice-bar.vue'
	import spaceSwiper from '@/components/space-swiper.vue'
	import cmdIcon from "@/components/cmd-icon/cmd-icon.vue"
	export default {
		components: {
			uniNavBar
		},
		components: {
			cmdIcon
		},
		components: {
			uniIcons
		},
		components: {
			uniNoticeBar
		},
		components: {
			spaceSwiper
		},

		data() {
			return {

			}
		},
		methods: {

		}
	}
</script>

<style>
	.example-body {
		width: 300px;

	}

	.input-uni-icon {
		position: absolute;
		top: 0px;
		left: 56px;
	}

	.nav-bar-input {
		color: #8f8f8f;
		background-color: #FAFAFA;
		/* width: 200px; */
		border: 1px solid #C0C0C0;
		border-radius: 30rpx
	}

	.nav-bar-input {
		/* padding-left: 20px; */
	}

	.content {
		width: 100%;
		height: 400rpx;
	}
	.content image{
		width: 95%;
		height: 395rpx;
		margin: 0px 0rpx 10rpx 20rpx;
		border-radius: 20rpx;
	}
	/* 方块内容 */
	.sp_text {
		width: 100%;
		height: 200rpx;
		padding-top: 20rpx;
		margin: 0 auto;

	}

	.square {
		width: 300rpx;
		height: 100%;
		background-color: #E15348;
		border-radius: 10rpx;
		float: left;
		margin: 0 20rpx 0 20rpx;
		color: #ffffff;
		text-align: center;
	}

	.sp_text p {
		font-size: 13px;
	}

	.text {
		width: 250rpx;
		height: 200rpx;
		margin: 30rpx 20rpx;
	}

	.square2 {
		width: 185rpx;
		height: 100%;
		background-color: #FF823F;
		border-radius: 10rpx;
		float: left;
		margin: 0 20rpx 0 0;
		color: #ffffff;
	}

	.square2 .text {
		width: 170rpx;
		height: 200rpx;
		margin: 30rpx 20rpx;
	}

	.square3 {
		width: 185rpx;
		height: 100%;
		background-color: #FFCA5E;
		border-radius: 10rpx;
		float: left;
		margin: 0 20rpx 0 0;
		color: #ffffff;
	}

	.square3 .text {
		width: 170rpx;
		height: 200rpx;
		margin: 30rpx 20rpx;
	}

	/* 字体轮播 */
	.font_sile {
		width: 100%;
		height: 100rpx;
		float: left;
	}

	.font_sile span {
		width: 160rpx;
		float: left;
		line-height: 90rpx;
		margin-left: 20rpx;
		color: #f30f31;
	}

	.uni-notice-bar {
		/* width: 300rpx; */
		float: left;
	}

	/* 拼团预售 */
	.Spell {
		width: 100%;
		height: 100rpx;
		float: left;
		line-height: 90rpx;
	}

	#sp {
		width: 200rpx;
		height: 100%;
		float: left;
		font-size: 37rpx;
		font-weight: 600;
		color: #000000;
		margin-left: 30rpx;
	}

	.Spell span {
		font-size: 30rpx;
		height: 100rpx;
		width: 300rpx;
		float: right;
		color: #CCCCCC;
		/* background-color: #000000; */
	}

	/* 商品轮播 */
	.goods_slie {
		width: 100%;
		height: 380rpx;
		float: left;
	}

	/* 商品列表 */
	.goods_list {
		width: 100%;
		height: 580rpx;
		float: left;
	}

	.row {
		width: 100%;
		height: 290rpx;
		margin: 0 auto;
	}

	.col {
		width: 31%;
		height: 290rpx;
		float: left;
		margin-left: 12.5rpx;
	}

	.col image {
		width: 80%;
		height: 150rpx;
		border-radius: 100rpx;
		margin: 10rpx 20rpx 0 20rpx;
	}

	.c_title {
		font-size: 30rpx;
		text-align: center;
	}

	.c_price {
		width: 100%;
		height: 50rpx;
		font-size: 26rpx;
		text-align: center;
		line-height: 50rpx;
		color: #c8c8c8;
	}

	.c_price span {
		font-size: 30rpx;
		color: #ff0000;
		float: left;
		margin-left: 30rpx;
	}

	.c_icon {
		float: right;
		margin-top: 10rpx;
	}

	.shangxin {
		width: 100%;
		height: 800rpx;
		/* background-color: #000000; */
		float: left;
		/* margin-top: 10rpx; */
	}
	.flex-item{
		width: 100%;
		height: 400rpx;
		}
	.flex_img{
		width: 260rpx;
		height: 260rpx;
		float: left;
		margin-left: 30rpx;
		
	}
	.flex_img image{
		width: 100%;
		height: 100%;
		border-radius: 100rpx;
	}
	.flex_text{
		width:400rpx;
		height: 260rpx;
		float: left;
		margin-left: 30rpx;
	}
	.f_t_title{
		font-size: 37rpx;
		color: #000000;
		line-height: 80rpx;
	}
	.flex_text p{
		font-size: 28rpx;
		color: #9B9B9B;
		line-height: 50rpx;
	}
	.flex_text_p{
		font-size: 35rpx;
		color: #fd1500;
		line-height: 100rpx;
	}
	.text_icon{
		float: right;
		margin-top: 35rpx;
		}
</style>
