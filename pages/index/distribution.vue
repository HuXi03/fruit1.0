<template>
	<view>
		<view class="dis_top">
			<navigator url="/pages/index/my" open-type="switchTab">
			<view class="top_icon"><cmd-icon type="chevron-left" size="30" color="#654321"></cmd-icon></view>
			</navigator>
		</view>
		<view class="shop_root">
			<view class="shop_root1">
				<view id="s_r1"><span>商品已在路上></span></view>
				<view class="s_r2"><span>12:35</span><view class="zhun">准送达</view></view>
				<view id="s_r3"><span>订单配送中 感谢您的耐心等待！</span></view>
			</view>
			<view class="shop_root2">
				<view class="shop_root2_i">
					<image src="../../static/waimai.jpg"></image>
				</view>
				<view class="shop_root2_t">
					<span id="name">大马哥</span><uni-icons type="phone-filled" size="20" color="#0000f4" style="float: right;"></uni-icons><br/>
					<span id="des">快马加鞭的配送小哥</span><span id="des" style="float: right;margin-top: 10rpx;">联系</span>
				</view>
			</view>
		</view>
		<view class="order1">
			<view class="o_detail">
					<image style="width: 80px;height: 80px;float: left;margin-top: 20rpx;" src="/static/pingguo.jpg"></image>
				<view class="o_detail_t">
					<span id="detail_text">法国嘎啦苹果*6 约800g</span><span class="detail_text_p">￥25</span>
				</view>
				<view class="o_detail_t1">
					<span id="detail_text1">规格：800g</span><span class="detail_text_p1">×1</span>
				</view>
			</view>
			<view class="o_detail">
					<image style="width: 80px;height: 80px;float: left;margin-top: 20rpx;" src="/static/bingtangcheng.jpg"></image>
				<view class="o_detail_t">
					<span id="detail_text">湖南麻阳冰糖橙*6 约500g</span><span class="detail_text_p">￥12.5</span>
				</view>
				<view class="o_detail_t1">
					<span id="detail_text1">规格：约500g/份</span><span class="detail_text_p1">×1</span>
				</view>
			</view>
			<view class="o_detail">
					<image style="width: 80px;height: 80px;float: left;margin-top: 20rpx;" src="/static/qicheng.jpg"></image>
				<view class="o_detail_t">
					<span id="detail_text">江西赣南脐橙*3 约500g</span><span class="detail_text_p">￥29</span>
				</view>
				<view class="o_detail_t1">
					<span id="detail_text1">规格：约500/份</span><span class="detail_text_p1">×2</span>
				</view>
			</view>
			<view class="shop_t">
				<span>配送费</span><span id="shop_t_p">￥0</span>
			</view>
			<view class="shop_t">
				<span>优惠</span><span id="shop_t_p">￥-10</span>
			</view>
			<view class="total_price"><span>总计￥132.50</span></view>
		</view>
		<view class="card1">
			<view class="card1_title">配送信息</view>
			<view class="card1_text">送达时间<span class="t_time">准送达 12:18</span></view>
			<view class="card1_text">收货地址<span class="t_time">海淀北二街8号中关村SOHO大厦26号</span><br/>
			<span class="t_time">小李子（先生） 1552****662</span>
			</view>
			<view class="card1_text">配送方式<span class="t_time">准送达</span></view>
		</view>
		<view class="card1">
			<view class="card1_title">订单信息</view>
			<view class="card1_text">订单号<span class="t_time">660201810263003168</span></view>
			<view class="card1_text">下单时间<span class="t_time">2018-01-26 10:21</span>
			</view>
			<view class="card1_text">支付方式<span class="t_time">快捷支付</span></view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
.dis_top{
	width: 100%;
	height: 350rpx;
	background-image: url(../../static/adress.jpg);
	
}
.top_icon{
	width: 40rpx;
	height: 40rpx;
	padding: 40rpx 50rpx;
}
.shop_root{
	width: 90%;
	height: 350rpx;
	margin: -80rpx 20rpx 20rpx 35rpx;
	border-radius: 20rpx;
	background-color: #ffffff;
	border: 1px solid #cacaca;
}
.shop_root1{
	width: 100%;
	height: 200rpx;
}
#s_r1{
	width: 300rpx;
	height: 70rpx;
	font-size: 40rpx;
	margin: 0 auto;
	line-height: 70rpx;
	}
#s_r1 span{
	/* margin-top: 50rpx; */
}
.s_r2{
	width: 250rpx;
	height: 50rpx;
	margin-left: 220rpx;
	float: left;
	}
.s_r2 span{
	color: #f90213;
	float: left;
	margin-right: 10rpx;
}
.zhun{
	width: 85rpx;
	height: 30rpx;
	font-size: 25rpx;
	margin-top: 10rpx;
	float: left;
	text-align: center;
	border:1.5px solid #fd1601;
	border-radius: 10rpx 0 10rpx 0;
	color: #fd1601;
}
#s_r3{
	width: 400rpx;
	height: 70rpx;
	font-size: 26rpx;
	margin: 0 auto;
	}
#s_r3 span{
	color: #a6a8b0;
	float: left;
	margin-right: 10rpx;
	
	}
.shop_root2{
	width: 100%;
	height: 100rpx;
	}
.shop_root2_i{
	width: 95rpx;
	height: 95rpx;
	border-radius: 50%;
	margin-left: 30rpx;
	float: left;
}
.shop_root2_i image{
	width: 100%;
	height: 100%;
	border-radius: 50%;
}
.shop_root2_t{
	width: 500rpx;
	height: 100%;
	float: left;
	margin-left: 20rpx;
}
#name{
	width: 100rpx;
	height: 40rpx;
	font-size: 34rpx;
	}
#des{
	font-size: 26rpx;
	color: #9c9c9c;
	margin-bottom: 20rpx;
}
/* 商品内容 */
.order1{
			width: 95%;
			height:100%;
			margin: 0 auto;
			background-color: #fcfcfc;
			border: 1px solid #e2e2e2;
			margin: 20rpx 20rpx 20rpx;
		}
		.o_detail{
			width: 100%;
			height: 200rpx;
		}
		.o_detail_t{
			width: 530rpx;
			height: 60rpx;
			float: left;
			margin-top: 50rpx;
			margin-left: 10rpx;
		}
		#detail_text{
			width:340rpx;
			height: 60rpx;
			font-size: 35rpx;
			font-weight: 800;
		}
		.detail_text_p{
			width:40rpx;
			height: 60rpx;
			font-size: 35rpx;
			color: #000000;
			float: right;
			margin-right: 50rpx;
		}
		#detail_text1{
			width:340rpx;
			height: 60rpx;
			color: #a6a6a6;
			font-size: 28rpx;
		}
		.detail_text_p1{
			width: 60rpx;
			height: 60rpx;
			color: #a6a6a6;
			float: right;
		}
		.o_detail_t1{
				width: 530rpx;
				height: 80rpx;
				margin-left: 10rpx;
				float: left;
			}
		.total{
			width: 100%;
			height: 170rpx;
		}
		.total p{
			width: 300rpx;
			height: 80rpx;
			font-size: 25rpx;
			color: #8c8c8c;
			float: right;
			margin-right: 10rpx;
			line-height: 100rpx;
		}
		#total_p{
			font-size: 30rpx;
			color: #000000;
			margin-left: 10rpx;
		}
		.ag{
			width: 200rpx;
			height: 60rpx;
			border-radius: 30rpx;
			background-color: #F6F6F6;
			font-size: 31rpx;
			float: left;
			line-height: 60rpx;
		/* 	margin-right: 20rpx; */
		}
		.sure{
			width: 200rpx;
			height: 60rpx;
			border-radius: 30rpx;
			background-color: #F6F6F6;
			font-size: 31rpx;
			float: right;
			line-height: 60rpx;
			
		}
		.butt{
			width: 430rpx;
			height: 70rpx;
			float: right;
			margin-right: 20rpx;
		}
		.shop_t{
			width: 100%;
			height: 100rpx;
			/* margin: 0 auto; */
			/* border: 1px solid #d3cbc2; */
		
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
		.total_price{
			width:100%;
			height: 100rpx;
			font-size: 30rpx;
			line-height: 100rpx;
		}
		.total_price span{
			float: right;
			margin-right: 20rpx;
		}
.card1{
		width: 95%;
		height: 350rpx;
		margin: 0 auto;
		background-color: #fcfcfc;
		border: 1px solid #e2e2e2;
		margin-bottom: 30rpx;
}
.card1_title{
	font-weight: 500;
	margin-left: 20rpx;
	height: 100rpx;
	line-height: 70rpx;
}
.card1_text{
	width: 100%;
	height: 90rpx;
	font-size: 30rpx;
	margin-left: 20rpx;
}
.t_time{
	float: right;
	margin-right: 30rpx;
	background-color: #fcfcfc;
}
</style>
