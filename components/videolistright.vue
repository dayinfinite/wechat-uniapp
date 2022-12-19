<template>
	<view class="listright">
		<view class="author-img">
			<image class="img" src="../static/logo.png" mode=""></image>
		</view>
		<view class="iconfont icon-anxin right-box"></view>
		<view class="number">123</view>
		<view class="iconfont icon-pinglun right-box"></view>
		<view class="number">123</view>
		<view class="iconfont icon-shoucang right-box"></view>
		<view class="number">123</view>
		<view class="iconfont icon-zhuanfa right-box"></view>
		<view class="number">123</view>
		<view class="around">
			<image class="img" src="../static/logo.png" mode=""></image>
		</view>
	</view>
</template>

<script>
	export default {
		name:"videolistright",
		data() {
			return {
				
			};
		}
	}
</script>

<style>
.img {
	height: 50px;
	width: 50px;
	border-radius: 50%;
}
.listright {
	width: 50px;
	margin: 0 auto;
}
.author-img {
	height: 50px;
	width: 50px;
	border-radius: 50%;
	border: 2px solid aliceblue;
}
.right-box {
	width: 50px;
	height: 40px;
	margin-top: 13px;
	text-align: center;
	line-height: 40px;
	color: aliceblue;
	font-size: 35px;
}
.number {
	font-size: 10px;
	text-align: center;
	color: aliceblue;
}
.around {
	margin-top: 15px;
	animation: rotate 1.5s linear 0.2s infinite;
	height: 50px;
	width: 50px;
}

@keyframes rotate {
	0% {
		transform: rotate(0deg);
	}
	100% {
		transform: rotate(350deg);
	}
}
</style>