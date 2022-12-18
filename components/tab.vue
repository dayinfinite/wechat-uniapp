<template>
	<view class="tab">
		<view class="tab-box">
			首页
		</view>
		<view class="tab-box">
			关注
		</view>
		<view class="tab-box">
			<view class="iconfont icon-jiahao icon-box">
			</view>
		</view>
		<view class="tab-box">
			消息
		</view>
		<view class="tab-box">
			我的
		</view>
	</view>
</template>

<script>
	export default {
		name:"tab",
		data() {
			return {
				
			};
		}
	}
</script>

<style>
.tab{
	height: 50px;
	width: 100%;
	position: fixed;
	bottom: 0;
	left: 0;
}
.tab-box {
	float: left;
	width: 20%;
	color: aliceblue;
	background-color: rgba(0,0,0,0);;
	text-align: center;
	height: 50px;
	line-height: 50px;
	font-size: 20px;
}
.icon-box {
	width: 60%;
	height: 30px;
	background-color: aliceblue;
	color: black;
	margin: 10px 20%;
	line-height: 30px;
	border-radius: 5px;
	font-size: 15px;
}
</style>