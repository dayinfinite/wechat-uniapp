<template>
	<view class="videoPlayer">
		<video id="myvideo" class="video" :src="video.src" :controls="true" 
		:autoplay="autoplay"
		@click="playerCurrent">
		</video>
	</view>
</template>

<script>
	var timer = null
	export default {
		name:"videoplayer",
		props: ['video', 'index'],
		data() {
			return {
				playerStatus: false,
				dbclick: false,
				autoplay: false
			};
		},
		onReady() {
			this.videoContext = uni.createVideoContext('myvideo', this)
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
				clearTimeout(timer)
				this.dbclick = !this.dbclick
				timer=setTimeout(() => {
					if(this.dbclick) {
						if(!this.playerStatus) {
							this.videoContext.play()
							this.playerStatus = true
						} else {
							this.videoContext.pause()
							this.playerStatus = false
						}
					} else {
						this.$emit('changeclick')
					}
					this.dbclick = false
				}, 300)
			},
			auto() {
				if(this.index === 0) {
					this.autoplay=true
				}
			}
		},
		created() {
			this.auto()
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