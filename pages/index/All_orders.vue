<template>
        <view>
			<view class="top">
				<navigator url="/pages/index/my" open-type="switchTab">
				   <uni-nav-bar left-icon="back"  title="全部订单"></uni-nav-bar>
				</navigator>
			</view>
                <view class="inv-h-w">
                        <view :class="['inv-h',Inv==0?'inv-h-se':'']" @click="Inv=0">全部</view>
                        <view :class="['inv-h',Inv==1?'inv-h-se':'']" @click="Inv=1">待支付</view>
						<view :class="['inv-h',Inv==2?'inv-h-se':'']" @click="Inv=2">待配送</view>
						<view :class="['inv-h',Inv==3?'inv-h-se':'']" @click="Inv=3">配送中</view>
						<view :class="['inv-h',Inv==4?'inv-h-se':'']" @click="Inv=4">待评价</view>
                </view>
                <view class="" v-show="Inv == 0">
                    <view class="order1">
						<uni-list>
							<uni-list-item leftText="准时达" rightText="配送中" title="约12:35送达" />
						</uni-list>
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
						<view class="total">
							<p>共3件商品<span id="total_p">合计￥88.60</span></p><br/>
							<view class="butt"><button class="ag">再来一单</button>
							<navigator url="/pages/index/sure_order" open-type="navigate">
							   <button class="sure">确认送达</button>
							</navigator>
							</view>
						</view>
						    </uni-list-item>
						</uni-list>
					</view>
					
					<!-- 第二单 -->
					<view class="order1">
						<uni-list>
							<uni-list-item rightText="自提配送中" title="约明日18:10送达" />
						</uni-list>
						<view class="o_detail">
								<image style="width: 80px;height: 80px;float: left;margin-top: 20rpx;" src="/static/huangjiaopingguo.jpg"></image>
							<view class="o_detail_t">
								<span id="detail_text">甘肃黄蕉苹果*6 约2斤</span><span class="detail_text_p">￥25</span>
							</view>
							<view class="o_detail_t1">
								<span id="detail_text1">规格：1kg/份</span><span class="detail_text_p1">×1</span>
							</view>
						</view>
						<view class="total">
							<p>共1件商品<span id="total_p">合计￥12.50</span></p><br/>
							<view class="butt"><button class="ag">再来一单</button>
							<navigator url="/pages/index/finish" open-type="navigate">
							<button class="sure">确认送达</button>
							</navigator>
							</view>
						</view>
						    </uni-list-item>
						</uni-list>
					</view>
					<view class="order1">
						<uni-list>
							<uni-list-item rightText="2017-12-26 12:42" title="订单已完成" />
						</uni-list>
						<view class="o_detail">
								<image style="width: 80px;height: 80px;float: left;margin-top: 20rpx;" src="/static/qicheng.jpg"></image>
								<image style="width: 80px;height: 80px;float: left;margin-top: 20rpx;margin-left: 20rpx;" src="/static/huangjiaopingguo.jpg"></image>
								<image style="width: 80px;height: 80px;float: left;margin-top: 20rpx;margin-left: 20rpx;" src="/static/mizao.jpg"></image>
								<image style="width: 80px;height: 80px;float: left;margin-top: 20rpx;margin-left: 20rpx;" src="/static/chelizi.jpg"></image>
						</view>
						<view class="total">
							<p>共6件商品<span id="total_p">合计￥96.60</span></p><br/>
							<view class="butt"><button class="ag">评价</button>
							<button class="sure">确认送达</button></view>
						</view>
						    </uni-list-item>
						</uni-list>
					</view>
                </view>
                <view class="" v-show="Inv == 1">
                        我是选项卡二
                </view>
				<view class="" v-show="Inv == 2">
				        我是选项卡3
				</view>
				<view class="" v-show="Inv == 3">
				        我是选项卡4
				</view>
				<view class="" v-show="Inv == 4">
				        我是选项卡5
				</view>
        </view>
</template>
 
<script>
	import uniNavBar from "@/components/uni-nav-bar/uni-nav-bar.vue"
	import uniList from '@/components/uni-list/uni-list.vue'
	import uniListItem from '@/components/uni-list-item/uni-list-item.vue'
        export default {
			components: {uniNavBar,uniList,
			uniListItem},
			
                data() {
                        return {
                                Inv:0
                        }
                },
                methods: {
                        changeTab(Inv){
                                that.navIdx = Inv;
                                 
                        },
                }
        }
</script>
         
<style>
        .inv-h-w{background-color: #FFFFFF;height: 100upx;display: flex;}
        .inv-h{font-size: 30upx;flex: 1;text-align: center;color: #323232;height: 100upx;line-height: 100upx;}
        .inv-h-se{color: #ff5c3c;border-bottom: 4upx solid #ff5c3c;}
        page{background-color: #F2F2F2;}
		.top{
			width: 100%;
			height: 90rpx;
		}
		.order1{
			width: 95%;
			height:100%;
			margin: 0 auto;
			background-color: #fcfcfc;
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
</style>