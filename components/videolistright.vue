<template>
	<view class="listright">
		<view class="author-img">
			<image class="img" src="../static/logo.png" mode=""></image>
			<view class="iconfont icon-jiahao add" v-show="show" @click="hidden"></view>
		</view>
		<view class="iconfont icon-anxin right-box" :style="anxincolor" @click="aixinColor"></view>
		<view class="number">{{video.likeCount}}</view>
		<view class="iconfont icon-pinglun right-box"></view>
		<view class="number">{{video.commentCount}}</view>
		<view class="iconfont icon-shoucang right-box" :style="shoucangcolor" @click="shoucangColor"></view>
		<view class="number">{{video.saveCount}}</view>
		<view class="iconfont icon-zhuanfa right-box"></view>
		<view class="number">{{video.shareCount}}</view>
		<view class="around">
			<image class="img" src="../static/logo.png" mode=""></image>
		</view>
	</view>
</template>

<script>
	export default {
		name:"videolistright",
		props: ["video"],
		data() {
			return {
				show: true,
				anxincolor: 'color:white;',
				shoucangcolor: 'color:white;'
			};
		},
		methods: {
			hidden() {
				this.show = false
			},
			aixinColor() {
				this.anxincolor = this.anxincolor==='color:white;'?'color:red;':'color:white;'
			},
			shoucangColor() {
				this.shoucangcolor = this.shoucangcolor==='color:white;'?'color:yellow;':'color:white;'
			},
			change() {
				this.anxincolor = "color:red;"
			}
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
	position: relative;
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
.add {
	width: 18px;
	height: 18px;
	border-radius: 50%;
	background-color: red;
	position: absolute;
	bottom: -9px;
	left: 16px;
	text-align: center;
	line-height: 18px;
	color: aliceblue;
	font-size: 10px;
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