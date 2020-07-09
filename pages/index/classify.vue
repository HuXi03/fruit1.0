<template>
	<view>
		<view class="example-body">
			<uni-nav-bar :fixed="false" type="search"  color="#424134" background-color="#FFFFFF" right-icon="menu" >
				<view class="nav-bar-input">
					<uni-icons class="input-uni-icon" type="search" size="25" color="#000000" />
					<input confirm-type="search" class="nav-bar-input" type="text" style="padding-left: 30px;" placeholder="搜索商品" @confirm="confirm">
					
				</view>
			</uni-nav-bar>
		</view>
		<view class="dmo">
			<view class="left">
				<scroll-view class="scroll" scroll-y="true">
					<view class="scroll-item" :class="current==index?'active':''" v-for="(item,index) in shop" :key="index" @click="scrol(index)">{{item}}</view>
				</scroll-view>
			</view>
			<view class="right">
				<scroll-view class="scroll_a" scroll-y="true" :scroll-into-view="'demo'+current" :scroll-with-animation="true">
					<view class="scroll-box"  id="demo0">
						<view class="list_img">
							<image src="../../static/shengnvguo.jpg"></image>
						</view>
					<navigator url="/pages/index/details" open-type="navigate">
						<view>
							<view style="padding-top: 30rpx;"><h4>海南陵水圣女果</h4></view>
							<view><p>酸酸甜甜根本停不下来</p></view>
							<view style="padding-top: 20rpx;"><span>￥34.0</span>/份</view>
						</view>
					</navigator>
					</view>
					<view class="scroll-box"  id="demo1">
						<view class="list_img">
							<image src="../../static/chelizi.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>智利黄金车厘子</h4></view>
							<view><p>再吃等一年！蜜一样的甜滋味</p></view>
							<view style="padding-top: 20rpx;"><span>￥80.0</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo2">
						<view class="list_img">
							<image src="../../static/qicheng.jpg"></image>
						</view>
					<navigator url="/pages/index/details" open-type="navigate">
						<view>
							<view style="padding-top: 30rpx;"><h4>江西脐橙*3 约500g</h4></view>
							<view><p>水分超多，脆嫩清香，浓甜可口</p></view>
							<view style="padding-top: 20rpx;"><span>￥29.0</span>/份</view>
						</view>
					</navigator>
					</view>
					<view class="scroll-box"  id="demo3">
						<view class="list_img">
							<image src="../../static/youtao.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>澳大利亚油桃*6个 约800g</h4></view>
							<view><p>不亚于水蜜桃的高颜值冬桃</p></view>
							<view style="padding-top: 20rpx;"><span>￥56.0</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo4">
						<view class="list_img">
							<image src="../../static/bingtangcheng.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>湖南麻阳冰糖橙*6个 约500g</h4></view>
							<view><p>好比冰糖的高甜度，细嫩可口</p></view>
							<view style="padding-top: 20rpx;"><span>￥12.5</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo5">
						<view class="list_img">
							<image src="../../static/mizao.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>台湾牛奶蜜枣*6个 约2斤</h4></view>
							<view><p>清脆可口，真的有奶香！</p></view>
							<view style="padding-top: 20rpx;"><span>￥12.5</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo6">
						<view class="list_img">
							<image src="../../static/qiyiguo.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>宜州奇异果/猕猴桃*6个 约2斤</h4></view>
							<view><p>猕猴喜食，故有诸名</p></view>
							<view style="padding-top: 20rpx;"><span>￥22.5</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo7">
						<view class="list_img">
							<image src="../../static/caomei.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>新鲜草莓*12个 约500g</h4></view>
							<view><p>猕猴喜食，故有诸名</p></view>
							<view style="padding-top: 20rpx;"><span>￥22.5</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo8">
						<view class="list_img">
							<image src="../../static/lanmei.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>可口蓝莓*20个 约500g</h4></view>
							<view><p>酸酸甜甜，故有诸名</p></view>
							<view style="padding-top: 20rpx;"><span>￥30.0</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo9">
						<view class="list_img">
							<image src="../../static/taoxingli.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>紫鲜葡萄 约500g</h4></view>
							<view><p>颗颗饱满，粒粒可口</p></view>
							<view style="padding-top: 20rpx;"><span>￥20.0</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo10">
						<view class="list_img">
							<image src="../../static/pingguo.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>紫鲜葡萄 约500g</h4></view>
							<view><p>颗颗饱满，粒粒可口</p></view>
							<view style="padding-top: 20rpx;"><span>￥20.0</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo11">
						<view class="list_img">
							<image src="../../static/li.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>紫鲜葡萄 约500g</h4></view>
							<view><p>颗颗饱满，粒粒可口</p></view>
							<view style="padding-top: 20rpx;"><span>￥20.0</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo12">
						<view class="list_img">
							<image src="../../static/xigua.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>紫鲜葡萄 约500g</h4></view>
							<view><p>颗颗饱满，粒粒可口</p></view>
							<view style="padding-top: 20rpx;"><span>￥20.0</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo13">
						<view class="list_img">
							<image src="../../static/xianggua.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>紫鲜葡萄 约500g</h4></view>
							<view><p>颗颗饱满，粒粒可口</p></view>
							<view style="padding-top: 20rpx;"><span>￥20.0</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo14">
						<view class="list_img">
							<image src="../../static/hamigua.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>紫鲜葡萄 约500g</h4></view>
							<view><p>颗颗饱满，粒粒可口</p></view>
							<view style="padding-top: 20rpx;"><span>￥20.0</span>/份</view>
						</view>
					</view>
					<view class="scroll-box"  id="demo15">
						<view class="list_img">
							<image src="../../static/guogan.jpg"></image>
						</view>
						<view>
							<view style="padding-top: 30rpx;"><h4>紫鲜葡萄 约500g</h4></view>
							<view><p>颗颗饱满，粒粒可口</p></view>
							<view style="padding-top: 20rpx;"><span>￥20.0</span>/份</view>
						</view>
					</view>
				</scroll-view>
			</view>
		</view>
		
	</view>
</template>

<script>
	import spaceSwiper from '../../components/space-swiper.vue'
	import uniNavBar from "@/components/uni-nav-bar/uni-nav-bar.vue"
	import uniIcons from "@/components/uni-icons/uni-icons.vue"
	
	export default {
		components: {uniNavBar},
		components: {uniIcons},
		components: {spaceSwiper},
		data() {
			return {
				current:0,
				/* arr:["A","B","C","D","D","D","D","D","D","D","D"], */
				shop:["今日优惠","进口鲜果","时令鲜果","今日鲜果","车厘子","柑橘橙柚","奇异果","草莓/蓝莓","葡萄/提子","桃杏李","苹果/李","瓜类","干果/零食"]
			}
		},
		methods: {
			scrol(num){
				this.current=num;
				console.log(this.current);
			}
		}
	}
</script>

<style>
/* 搜索 */
.example-body{
	width: 300px;
	
		}
.input-uni-icon{
	position: absolute;
	top: 0px;
	left: 55px;	
	}
.nav-bar-input{
	color:#8f8f8f;
	background-color:#FAFAFA;
	width: 500rpx;
	height: 50rpx;
	border-radius: 30rpx
	}
.nav-bar-input{
	/* padding-left: 20px; */
}
.content{
	margin-top: 10px;
}
.dmo{
	height: 100%;
	display: flex;
	}
.scroll{
	width: 100px;
	height: 100%;
}
.scroll_a{
	width: 270px;
	height: 650px;
}
.active{
	/*  border-left: #007AFF 2px solid;*/
	background-color: #FAFAFA;
}
.scroll-item{
	width: 100%;
	height: 100rpx;
	line-height: 100rpx;
	text-align: center;
	font-size: 15px;
}
.scroll-box{
	width: 100%;
	height: 200rpx;
	background-color: #FAFAFA;
	margin: 10rpx 10rpx 10rpx 0;
	font-size: 15px;
}
.scroll-box p{
	color: #79747f;
	font-size: 24rpx;
}
.scroll-box span{
	color: #e80000;
	font-size: 35rpx;
}
.list_img{
	width: 190rpx;
	height: 190rpx;
	float: left;
	margin: 10rpx 10rpx;
	
	}
.list_img image{
	width: 100%;
	height: 100%;
	border-radius: 70rpx;
}
</style>
