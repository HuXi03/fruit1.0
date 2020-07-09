<template>
	<view>
		<view class="top">
			<navigator url="/pages/index/classify" open-type="switchTab">
			   <uni-nav-bar left-icon="back"></uni-nav-bar>
			</navigator>
		</view>
		<view class="details_img">
			<image src="../../static/bingtangcheng.jpg"></image>
		</view>
		<view class="details_inc">
			<p>广东四会砂糖橘 越两斤装</p>
			<span id="jieshao">比水果店性价比还高！味甜、易剥还新鲜！</span>
			<span id="goods_p">￥26.0<span id="fen">/份</span></span><span id="shengyu">仅剩500份</span>
			<uni-list class="list_all">
				<uni-list-item rightText="送至" title="背景海淀区中关村SOHO大厦16层1006" note="现在下单 最快今天19:45前送达" />
				<uni-list-item title="商品评价(10260)" note="产地直供,以为会是小橘子,结果很大,味道也挺不错..." />
			</uni-list>
		</view>
		<view class="take_o">
			<view class="take_o_t">——鲜果采摘——</view>
			<view class="take_o_d">
				<view class="take_o_c">
					<span id="take_o_c_l" style="padding: 30rpx;">产地   </span><span  id="take_o_c_r">江西省南丰县</span><br/>
					<span id="take_o_c_l">采摘日期</span><span id="take_o_c_r">2018.01.26</span><br/>
					<span id="take_o_c_l">天气状况</span><span id="take_o_c_r">晴 16°C</span><br/>
					<span id="take_o_c_l">运输方式</span><span id="take_o_c_r">冷链保鲜运输</span>
				</view>
				<view class="details_i">
					<image src="../../static/detail.png"></image>
				</view>
			</view>
		</view>
		<view class="goods-carts">
			<uni-goods-nav :fill="true" :button-group="buttonGroup" @click="onClick" @buttonClick="buttonClick" />
		</view>
	</view>
</template>

<script>
	import uniList from '@/components/uni-list/uni-list.vue'
	import uniListItem from '@/components/uni-list-item/uni-list-item.vue'
	import uniCard from '@/components/uni-card/uni-card.vue'
	export default {
		components: {
			uniList,
			uniListItem,
			uniCard
		},
		data() {
			return {
				options: [{
					icon: 'headphones',
					text: '客服'
				}, {
					icon: 'shop',
					text: '店铺',
					info: 2,
					infoBackgroundColor: '#007aff',
					infoColor: "#f5f5f5"
				}],
				buttonGroup: [{
						text: '加入购物车',
						backgroundColor: '#ffa200',
						color: '#fff'
					},
					{
						text: '立即购买',
						backgroundColor: '#ff0000',
						color: '#fff'
					}
				]
			}
		},
		onLoad() {},
		methods: {
			onClick(e) {
				uni.showToast({
					title: `点击${e.content.text}`,
					icon: 'none'
				})
			},
			buttonClick(e) {
				console.log(e)
				this.options[2].info++
			}
		}
	}
</script>

<style>
	.details_img {
		width: 100%;
		height: 900rpx;
	}

	.details_img image {
		width: 100%;
		height: 100%;
	}

	.details_inc {
		width: 100%;
		height: 480rpx;
		border: 1px solid #a5afb8;
		border-radius: 100rpx;
	}

	.details_inc p {
		color: #000000;
		font-size: 40rpx;
		margin: 40rpx 0 0 40rpx;
	}

	#jieshao {
		font-size: 30rpx;
		color: #a2a8aa;
		margin: 40rpx 40rpx 0 40rpx;
	}

	#goods_p {
		color: #e22652;
		font-size: 37rpx;
		margin-left: 40rpx;
	}

	#fen {
		color: #8b8e8f;
		font-size: 28rpx;
	}

	#shengyu {
		float: right;
		color: #8b8e8f;
		font-size: 28rpx;
		line-height: 50rpx;
		margin: 13rpx 80rpx 0 0;
	}

	.list_all {
		width: 100%;
		height: 30rpx;
	}
	
	.take_o{
		width: 100%;
		height: 790rpx;
		float: left;
		}
	.take_o_t{
		width: 100%;
		height: 90rpx;
		text-align: center;
		line-height: 90rpx;
	}
	.take_o_d{
		width: 90%;
		height: 600rpx;
		margin: 0 auto;
		
	}
	.take_o_c{
		width: 70%;
		height:200rpx;
		font-size: 30rpx;
		margin: 0 auto;
		padding-top: 30rpx;
		}
	#take_o_c_l{
		width: 30%;
		height: 60rpx;
		margin: 20rpx 30rpx;
	}
	.details_i{
		width: 80%;
		height: 400rpx;
		
		margin: 0 auto;
		}
	.details_i image{
		width: 100%;
		height: 100%;
		border-radius: 50rpx;
	}	
	.goods-carts {
		/* #ifndef APP-NVUE */
		display: flex;
		/* #endif */
		flex-direction: column;
		position: fixed;
		left: 0;
		right: 0;
		bottom: 0;
	}

</style>
