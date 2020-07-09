<template>
	<view class="all">
		<view class="icon_s_n">
			<image class="img_l" src="../../static/setting.png"></image>
			<image class="img_r" src="../../static/news.png"></image>
		</view>
		<view class="info">
			<view class="info_top">
				<view class="info_top_l">
					<image src="../../static/title_img.jpg"></image>
					<view class="font">Hu晓</view>
				</view>
				<view class="info_top_r">
					<image src="../../static/二维码.png"></image>
				</view>
			</view>
			<view class="info_buttom">
				<view class="cost">
					<span>
						<h5>0</h5>
						<p>账户余额</p>
					</span>
				</view>
				<view class="cost">
					<span>
						<h5>0</h5>
						<p>优惠券</p>
					</span>
				</view>
				<view class="cost">
					<span>
						<h5>0</h5>
						<p>账户积分</p>
					</span>
				</view>
			</view>
		</view>
		<view class="take_g">
			<view class="take_g0">
				<image src="../../static/待支付.png"></image>
				<p>待支付</p>
			</view>
			<view class="take_g1">
				<image src="../../static/待配送.png"></image>
				<p>待配送</p>
			</view>
			<view class="take_g2">
				<image src="../../static/配送中.png"></image>
				<p>配送中</p>
			</view>
			<view class="take_g3">
				<image src="../../static/待评价.png"></image>
				<p>待评价</p>
			</view>
			<view class="take_g4">
				<navigator url="/pages/index/All_orders" open-type="navigate">
				<image src="../../static/全部订单.png"></image>
				<p>全部订单</p>
				</navigator>
			</view>
		</view>
		<uni-list class="list_all">
			<uni-list-item :show-extra-icon="true" :extra-icon="extraIcon1" title="我的收藏" />
			<uni-list-item :show-extra-icon="true" :extra-icon="extraIcon2" title="优惠福利" />
			<uni-list-item :show-extra-icon="true" :extra-icon="extraIcon3" title="会员中心" />
		</uni-list>
		<uni-list class="list_all">
			<uni-list-item :show-extra-icon="true" :extra-icon="extraIcon4" title="地址管理" />
			<uni-list-item :show-extra-icon="true" :extra-icon="extraIcon5" title="门店/自提点查询" />
			<uni-list-item :show-extra-icon="true" :extra-icon="extraIcon6" title="客服帮助" />
			<uni-list-item :show-extra-icon="true" :extra-icon="extraIcon7" title="设置" />
		</uni-list>
	</view>
</template>

<script>
	import uniSection from '@/components/uni-section/uni-section.vue'
	import uniList from '@/components/uni-list/uni-list.vue'
	import uniListItem from '@/components/uni-list-item/uni-list-item.vue'
	export default {
		components: {
			uniSection,
			uniList,
			uniListItem
		},
		data() {
			return {
				extraIcon1: {
					color: '#ff3a13',
					size: '22',
					type: 'heart-filled'
				},
				extraIcon2: {
					color: '#ff3a13',
					size: '22',
					type: 'locked-filled'
				},
				extraIcon3: {
					color: '#ff3a13',
					size: '22',
					type: 'personadd-filled'
				},
				extraIcon4: {
					color: '#007aff',
					size: '22',
					type: 'location-filled'
				},
				extraIcon5: {
					color: '#007aff',
					size: '22',
					type: 'shop'
				},
				extraIcon6: {
					color: '#007aff',
					size: '22',
					type: 'headphones'
				},
				extraIcon7: {
					color: '#007aff',
					size: '22',
					type: 'gear-filled'
				},
			}
		},
		methods: {
			switchChange(e) {
				uni.showToast({
					title: 'change:' + e.value,
					icon: 'none'
				})
			}
		}
	}
</script>

<style>
.all{
	width: 100%;
	height: 100%;
	background-image: url(../../static/bg.png);
	}
.icon_s_n{
	width: 92%;
	height: 70rpx;
	margin: 0rpx 30rpx;
	float: left;
}
.img_l{
	width: 50rpx;
	height: 50rpx;
	float: left;
	margin: 10rpx 20rpx;
}
.img_r{
	width: 50rpx;
	height: 50rpx;
	float: right;
	margin: 10rpx 20rpx;
}
.info{
	width: 92%;
	height: 270rpx;
	margin: 10rpx 30rpx;
	background-color: #FAFAFA;
	border-radius: 15rpx;
	float: left;
}
.info_top{
	width: 100%;
	height: 160rpx;
	float: left;
	/* margin:10rpx 10rpx */
}
.info_top_l{
	width: 50%;
	height: 90%;
	float: left;
	margin:10rpx 10rpx
}
.info_top_l image{
	width: 140rpx;
	height: 140rpx;
	border-radius: 15px;
	float: left;
}
.font{
	width: 100rpx;
	float: left;
	line-height: 150rpx;
	padding-left: 20rpx;
}
.info_top_r{
	width: 10%;
	height: 45%;
	float: right;
	margin:50rpx 50rpx
}
.info_top_r image{
	width: 60rpx;
	height: 60rpx;
}
.info_buttom{
	width: 100%;
	height: 100rpx;
	float: left;
	}
.cost{
	width: 30%;
	height: 100%;
	float: left;
	margin: 0 10rpx;
	text-align: center;
}
.cost p{
	font-size: 30rpx;
}
.take_g{
	width: 92%;
	height:150rpx;
	margin: 10rpx 30rpx;
	background-color: #FAFAFA;
	border-radius: 15rpx;
	float: left;
}
.take_g0{
	width: 20%;
	height: 100%;
	/* background-color: #032F62; */
	float: left;
	font-size: 14px;
	text-align: center;
}
.take_g0 image{
	width: 70rpx;
	height: 70rpx;
	margin:10rpx 0rpx;
}
.take_g1{
	width: 20%;
	height: 100%;
	/* background-color: #032F62; */
	float: left;
	font-size: 14px;
	text-align: center;
}
.take_g1 image{
	width: 90rpx;
	height: 90rpx;
	/* margin-top: 10rpx; */
}
.take_g2{
	width: 20%;
	height: 100%;
	/* background-color: #032F62; */
	float: left;
	font-size: 14px;
	text-align: center;
}
.take_g2 image{
	width: 80rpx;
	height: 80rpx;
	margin-top: 10rpx;
}
.take_g3{
	width: 20%;
	height: 100%;
	/* background-color: #032F62; */
	float: left;
	font-size: 14px;
	text-align: center;
}
.take_g3 image{
	width: 80rpx;
	height: 80rpx;
	margin-top: 10rpx;
}
.take_g4{
	width: 20%;
	height: 100%;
	/* background-color: #032F62; */
	float: left;
	font-size: 14px;
	text-align: center;
}
.take_g4 image{
	width: 80rpx;
	height: 80rpx;
	margin-top: 10rpx;
}
.list_all{
	width: 100%;
	height: 100%;
	margin: 20rpx 0rpx;
	background-color:#FAFAFA;
}
</style>