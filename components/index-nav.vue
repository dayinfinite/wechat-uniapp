<template>
	<view class="indexnav">
		<view class="iconfont icon-sousuo icon"></view>
		<view class="middle">
			<view class="text">
				推荐
			</view>
			<view class="text">
				同城
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		name:"index-nav",
		data() {
			return {
				
			};
		}
	}
</script>

<style>
.indexnav {
	width: 100%;
	position: fixed;
	top: 25px;
	left: 0;
	height: 35px;
	line-height: 35px;
	margin: 0 auto;
	background-color: rgba(0,0,0,0);;
	z-index: 19;
}
.icon {
	position: absolute;
	top: 0;
	left: 0;
	color: aliceblue;
	width: 20%;
	text-align: center;
	font-size: 20px;
}
.middle {
	text-align: center;
	
}
.text {
	display: inline;
	color: aliceblue;
	margin: 0 10px;
}
</style>