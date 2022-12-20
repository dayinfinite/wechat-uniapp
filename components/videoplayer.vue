<template>
	<view class="videoPlayer">
		<video id="myvideo" class="video" :src="video.src" :controls="true" @click="playerCurrent">
		</video>
	</view>
</template>

<script>
	export default {
		name:"videoplayer",
		props: ['video'],
		data() {
			return {
				playerStatus: false
			};
		},
		onReady() {
			this.videoContext = uni.createVideoContext('myvideo', this)
			console.log('aaa')
		},
		methods: {
			player() {
				if(!this.playerStatus) {
					this.videoContext.seek(0)
					this.videoContext.play()
					this.playerStatus = true
				}
			},
			pause() {
				if(this.playerStatus) {
					this.videoContext.pause()
					this.playerStatus = false
				}
			},
			playerCurrent() {
				if(!this.playerStatus) {
					this.videoContext.play()
					this.playerStatus = true
				} else {
					this.videoContext.pause()
					this.playerStatus = false
				}
			}
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