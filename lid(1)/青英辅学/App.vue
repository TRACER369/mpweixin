<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
			// 这里检查下小程序环境
			console.log('运行环境：', uni.getSystemInfoSync())
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
	/*每个页面公共css */
	@import './static/css/iconfont.css';
	
	/* 全局样式 */
	page {
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
		background-color: #f5f5f5;
		font-size: 28rpx;
		color: #333;
	}
	
	/* 清除浮动 */
	.clearfix:after {
		content: "";
		display: block;
		clear: both;
	}
	
	/* 通用边距 */
	.margin-top {
		margin-top: 20rpx;
	}
	
	.margin-bottom {
		margin-bottom: 20rpx;
	}
	
	/* 通用圆角 */
	.radius {
		border-radius: 8rpx;
	}
	
	/* 通用阴影 */
	.shadow {
		box-shadow: 0 2rpx 10rpx rgba(0, 0, 0, 0.05);
	}
	
	/* 修复容器样式 */
	.container {
		width: 100%;
		min-height: 100vh;
	}
</style>
