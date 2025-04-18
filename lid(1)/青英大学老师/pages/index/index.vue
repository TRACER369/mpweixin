<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{ title }}</text>
		</view>
		<button type="primary" @click="goToTeacher">进入青英大学老师页面</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '青英大学老师应用'
			}
		},
		onLoad() {
			// 不使用自动跳转
			console.log('Index page loaded');
		},
		methods: {
			goToTeacher() {
				try {
					// 使用switchTab跳转到tabBar页面
					uni.switchTab({
						url: '/pages/teacher/teacher',
						success: function() {
							console.log('跳转成功');
						},
						fail: (err) => {
							console.error('Navigation failed:', err);
							// 显示错误提示
							uni.showToast({
								title: '跳转失败：' + JSON.stringify(err),
								icon: 'none',
								duration: 3000
							});
						}
					});
				} catch (e) {
					console.error('Navigation error:', e);
				}
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
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
		margin-bottom: 30rpx;
	}

	.title {
		font-size: 36rpx;
		color: #333;
	}
</style>
