<template>
	<view class="videoPlayer">
		<video class="video"  :src="video.src" :controls="true">
		</video>
	</view>
</template>

<script>
	export default {
		name:"videoplayer",
		props: ['video'],
		data() {
			return {
				
			};
		}
	}
</script>

<style>
.videoPlayer {
	height: 100%;
	width: 100%;
}
.video {
	height: 100%;
	width: 100%;
}
</style>