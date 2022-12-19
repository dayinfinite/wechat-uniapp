<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	html, body {
		width: 100%;
		height: 100%;
	}
	/*每个页面公共css */
	@font-face {
	  font-family: "iconfont"; /* Project id 3830608 */
	  src: url('//at.alicdn.com/t/c/font_3830608_ht4zzjr18q5.woff2?t=1671279154874') format('woff2'),
       url('//at.alicdn.com/t/c/font_3830608_ht4zzjr18q5.woff?t=1671279154874') format('woff'),
       url('//at.alicdn.com/t/c/font_3830608_ht4zzjr18q5.ttf?t=1671279154874') format('truetype');
	}
	
	@font-face {
	  font-family: 'iconfont';  /* Project id 3830713 */
	  src: url('//at.alicdn.com/t/c/font_3830713_wk8zg7v7ng.woff2?t=1671285388749') format('woff2'),
	       url('//at.alicdn.com/t/c/font_3830713_wk8zg7v7ng.woff?t=1671285388749') format('woff'),
	       url('//at.alicdn.com/t/c/font_3830713_wk8zg7v7ng.ttf?t=1671285388749') format('truetype');
	}
	
	/* CDN 服务仅供平台体验和调试使用，平台不承诺服务的稳定性，企业客户需下载字体包自行发布使用并做好备份。 */
	@font-face {
	  font-family: 'iconfont';  /* Project id 3830608 */
	  src: url('//at.alicdn.com/t/c/font_3830608_imo7wk6kufd.woff2?t=1671471501234') format('woff2'),
	       url('//at.alicdn.com/t/c/font_3830608_imo7wk6kufd.woff?t=1671471501234') format('woff'),
	       url('//at.alicdn.com/t/c/font_3830608_imo7wk6kufd.ttf?t=1671471501234') format('truetype');
	}
	
	.iconfont {
	  font-family: "iconfont" !important;
	  font-size: 16px;
	  font-style: normal;
	  -webkit-font-smoothing: antialiased;
	  -moz-osx-font-smoothing: grayscale;
	}
	
	.icon-jiahao:before {
	  content: "\e614";
	}
	.icon-sousuo:before {
	  content: "\eafe";
	}
	.icon-anxin:before {
	  content: "\e8ab";
	}
	.icon-pinglun:before {
		content: "\e615";
	}
	.icon-shoucang:before {
		content: "\e8b9";
	}
	.icon-zhuanfa:before {
		content: "\e633";
	}
</style>
