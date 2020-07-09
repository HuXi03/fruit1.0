<template>
	<view>
		<view class="top">
			<navigator url="/pages/index/shopping" open-type="switchTab">
			   <uni-nav-bar left-icon="back"  title="确认订单"></uni-nav-bar>
			</navigator>
		</view>
		<view class="card1">
			<uni-list class="list_all">
				<view class="method"><span>送货方式</span><view class="me_b"><button style="background-color:#c5010b;margin-right:10rpx;color:#ffffff;">配送</button><button>自提</button></view></view>
				<uni-list-item rightText="送至" title="北京海淀区中关村SOHO大厦16层1006" note="李(先生) 1552****668" />
				<uni-list-item title="约12:35送达" rightText="[可选送时段]" />
			</uni-list>
		</view>
		<view class="card2">
			<image class="card2_img" src="../../static/bingtangcheng.jpg"></image>
			<image class="card2_img" src="/static/huangjiaopingguo.jpg"></image>
			<image class="card2_img" src="/static/qicheng.jpg"></image>
			<image class="card2_img" src="/static/qiyiguo.jpg"></image>
			<cmd-icon class="card_icon" type="chevron-right" size="30" color="#beb8b6"></cmd-icon>
			<view><span id="card_p">￥12.5</span><span id="card_p">￥12.5</span><span id="card_p">￥12.5</span><span id="card_p">￥12.5</span></view>
			<view class="card2p"><span id="card_p2">×1</span><span id="card_p2">×2</span><span id="card_p2">×1</span><span id="card_p2">×1</span><span id="totol_c">共四件</span></view>
			<view class="shop_t">
				<span>商品总额</span><span id="shop_t_p">￥131.5</span><br/>
				<span>配送费<span style="color: #bdbdbd;font-size: 27rpx;">实付满30元免配送费</span></span><span id="shop_t_p">￥0</span>
			</view>
			<view class="total_price"><span>总计￥91.40</span></view>
			<uni-list class="list_all">
				<uni-list-item rightText="￥-40" title="优惠" />
			</uni-list>
			<uni-list class="list_all">
				<uni-list-item rightText="不开发票" title="发票" />
			</uni-list>
		</view>
		<view class="footer">
			<navigator url="/pages/index/finish" open-type="navigate">
			<button>去支付：￥91.40</button>
			</navigator>
		</view>
	</view>
</template>

<script>
	import cmdIcon from "@/components/cmd-icon/cmd-icon.vue"
	import uniList from '@/components/uni-list/uni-list.vue'
	import uniListItem from '@/components/uni-list-item/uni-list-item.vue'
	export default {
		components: {
		cmdIcon,
		uniList,
		uniListItem,},
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
.card1{
	width: 95%;
	height: 100%;
	margin: 0 auto;
	border: 1px solid #d3cbc2;
	border-radius:10rpx 10rpx 0 0;
	margin-bottom: 20rpx;
	/* margin: 30rpx 30rpx 30rpx; */
}
.list_all{
	/* margin-top: 20rpx; */
}
.method{
	width: 100%;
	height: 100rpx;
	border-radius: 10rpx 10rpx 0rpx 0rpx;
}
.method span{
	width: 150rpx;
	height: 40rpx;
	font-size: 30rpx;
	font-weight: 700;
	line-height: 40rpx;
	float: left;
	margin-top: 30rpx;
	margin-left: 25rpx;
}
.me_b{
	width: 300rpx;
	height: 40rpx;
	margin-top: 30rpx;
	float: right
}
.me_b button{
	width: 130rpx;
	height: 100%;
	border-radius: 40rpx;
	font-size: 28rpx;
	line-height: 35rpx;
	float: left;
	background-color: #FAFAFA;
}
.card2{
	width: 95%;
	height: 300rpx;
	margin: 0 auto;
	border: 1px solid #d3cbc2;	/* border-radius: 50rpx 50rpx 0rpx 0rpx; */	margin-bottom: 20rpx;
}
.card2_img{
	width: 70px;
	height: 70px;
	float: left;
	margin-top: 20rpx;
	margin-left: 20rpx;
	border-radius: 50rpx;
}
.card_icon{
	margin-top: 60rpx;
}
#card_p{
	width: 20rpx;
	height: 60rpx;
	font-size: 30rpx;
	text-align: center;
	margin: 10rpx 45rpx 0 30rpx;
}
.card2p{
	
	margin-left: 20rpx;
}
#card_p2{
	width: 10rpx;
	height: 60rpx;
	font-size: 30rpx;
	text-align: center;
	color: #b0b0b0;
	margin: 50rpx 95rpx 0 30rpx;
	}
#totol_c{
	float: right;
	color: #b0b0b0;
	font-size: 25rpx;
}
.shop_t{
	width: 100%;
	margin-top: 40rpx;
	height: 150rpx;
	/* margin: 0 auto; */
	border: 1px solid #d3cbc2;

}
.shop_t span{
	font-size: 35rpx;
	line-height: 70rpx;
	margin-left: 20rpx;
}
#shop_t_p{
	float: right;
	margin-right: 30rpx;
}
.list_all{
	/* width: 100%;
	margin-top: 40rpx;
	height: 150rpx;
	/* margin: 0 auto;  */
	/* border-left: 1px solid #d3cbc2;
	border-right: 1px solid #d3cbc2;
	border-bottom:  1px solid #d3cbc2; */
}
.total_price{
	width:100%;
	height: 100rpx;
	border: 1px solid #d3cbc2;
	font-size: 30rpx;
	line-height: 100rpx;
}
.total_price span{
	float: right;
	margin-right: 20rpx;
}
.footer{
	/* width: 100%;
	height: 60rpx;
	border: 1rpx; */
}
.footer button{
	width: 500rpx;
	font-size: 30rpx;
	background-color: #f90019;
	color: #fdfdfd;
	border-radius: 50rpx;
	position: fixed;
	bottom: 0;
	margin-left: 120rpx;
}
</style>
