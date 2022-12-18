<template>
	<view class="videolist">
		<view class="swiper-video">
			<swiper class="swiper" :vertical="true">
				<swiper-item v-for="item of videos" :key="item.key">
					<view class="swiper-item" style="color: aliceblue;">
						<videoplayer :video="item"></videoplayer>
					</view>
				</swiper-item>
			</swiper>
		</view>
	</view>
</template>

<script>
	import videoplayer from '../components/videoplayer.vue'
	export default {
		name:"video-list",
		props: ["list"],
		components: {
			videoplayer
		},
		data() {
			return {
				videos: []
			};
		},
		watch: {
			list() {
				this.videos = this.list
			}
		}
	}
</script>

<style>
.videolist {
	height: 100%;
	width: 100%;
	z-index: 21;
}
.swiper-video {
	height: 100%;
	width: 100%;
}
.swiper {
	height: 100%;
	width: 100%;
}
.swiper-item {
	height: 100%;
	width: 100%;
}
</style>