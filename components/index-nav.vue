<template>
	<view class="indexnav">
		<view class="iconfont icon-sousuo icon"></view>
		<view></view>
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
	top: 0;
	left: 0;
	height: 35px;
	line-height: 35px;
	margin: 0 auto;
	background-color: black;
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
</style>