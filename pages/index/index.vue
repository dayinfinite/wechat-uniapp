<template>
	<view class="content">
		<indexnav></indexnav>
		<videolist :list="list"></videolist>
		<tab></tab>
	</view>
</template>

<script>
	import tab from '../../components/tab.vue'
	import indexnav from '../../components/index-nav.vue'
	import videolist from '../../components/video-list.vue'
	export default {
		components: {
			tab,
			indexnav,
			videolist
		},
		data() {
			return {
				title: 'Hello',
				list: []
			}
		},
		onLoad() {
			this.getVideos()
		},
		methods: {
			getVideos() {
				var that=this;
				uni.request({
					url: "http://127.0.0.1:5080/videos.json",
					success(res) {
						that.list = res.data.list
						// console.log(that.list)
					}
				})
			}
		}
	}
</script>

<style>
	.content {
		/* display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center; */
		height: 100%;
		width: 100%;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
