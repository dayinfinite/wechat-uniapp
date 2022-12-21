<template>
	<view class="videolist">
		<view class="swiper-video">
			<swiper 
			class="swiper" 
			:vertical="true" 
			@change="change"
			@touchstart="touchstart"
			@touchend="touchend"
			>
				<swiper-item v-for="(item, index) of videos" :key="item.key">
					<view class="swiper-item" style="color: aliceblue;">
						<videoplayer @changeclick="changeClick" ref="player" :video="item" :index="index"></videoplayer>
					</view>
					<view class="listleft">
						<videolistleft :video="item"></videolistleft>
					</view>
					<view class="listright">
						<videolistright :video="item" ref="right"></videolistright>
					</view>
				</swiper-item>
			</swiper>
		</view>
	</view>
</template>

<script>
	import videoplayer from '../components/videoplayer.vue'
	import videolistleft from '../components/videolistleft.vue'
	import videolistright from '../components/videolistright.vue'
	var time = null
	export default {
		name:"video-list",
		props: ["list"],
		components: {
			videoplayer,
			videolistleft,
			videolistright
		},
		data() {
			return {
				videos: [],
				pagestartY: 0,
				pageendY: 0,
				page: 0
			};
		},
		watch: {
			list() {
				this.videos = this.list
			}
		},
		methods: {
			change(res) {
				this.page = res.detail.current
				clearTimeout(time)
				time=setTimeout(()=> {
					if(this.pagestartY < this.pageendY) {
						this.$refs.player[this.page].player()
						this.$refs.player[this.page + 1].pause()
						this.pagestartY=0
						this.pageendY=0
					} else {
						this.$refs.player[this.page].player()
						this.$refs.player[this.page - 1].pause()
						this.pagestartY=0
						this.pageendY=0
					}
				},1)
				
			},
			touchstart(res) {
				this.pagestartY = res.changedTouches[0].pageY
			},
			touchend(res) {
				this.pageendY = res.changedTouches[0].pageY
			},
			changeClick() {
				this.$refs.right[this.page].change()
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
.listleft {
	z-index: 20;
	position: absolute;
	bottom: 50px;
	left: 10px;
}
.listright {
	z-index: 20;
	position: absolute;
	bottom: 50px;
	right: 10px;
}
</style>