<template>
	<view class="videolistleft">
		<view class="author">
			张三
		</view>
		<view class="title1">
			抖音，记录美好生活
		</view>
		<view class="box">
			<view class="music">
				@抖音，记录美好生活@抖音，记录美好生活
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name:"videolistleft",
		data() {
			return {
				
			};
		}
	}
</script>

<style>
.videolistleft {
	height: 150px;
	margin-left: 10px;
	color: aliceblue;
	width: 120px;
}
.author {
	height: 35px;
	line-height: 35px;
	font-size: 15px;
}
.title1 {
	line-height: 15px;
	font-size: 12px;
	width: 100%;
}
.box {
	width: 100px;
	overflow: hidden;
}
.music {
	height: 35px;
	line-height: 35px;
	font-size: 12px;
	width: 140px;
	animation: music 4s linear 0.2s infinite;
}
@keyframes music {
	0% {
		transform: translate3d(80%, 0, 0);
	}
	100% {
		transform: translate3d(-80%, 0, 0);
	}
}
</style>