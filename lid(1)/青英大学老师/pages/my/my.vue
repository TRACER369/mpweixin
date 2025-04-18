<template>
	<view class="container">
		<!-- 顶部用户信息 -->
		<view class="user-info">
			<view class="avatar-container">
				<image src="/static/icons/user-avatar.png" class="avatar"></image>
			</view>
			<view class="user-details">
				<text class="username">用户名</text>
				<text class="user-id">ID: 123456</text>
			</view>
			<view class="settings">
				<image src="/static/icons/settings.png" class="settings-icon"></image>
			</view>
		</view>
		
		<!-- 数据统计 -->
		<view class="stats">
			<view class="stat-item">
				<text class="stat-number">0</text>
				<text class="stat-label">收藏</text>
			</view>
			<view class="stat-item">
				<text class="stat-number">0</text>
				<text class="stat-label">关注</text>
			</view>
			<view class="stat-item">
				<text class="stat-number">0</text>
				<text class="stat-label">历史</text>
			</view>
		</view>
		
		<!-- 选项列表 -->
		<view class="options-list">
			<view class="option-item">
				<image src="/static/icons/notification.png" class="option-icon"></image>
				<text class="option-text">消息通知</text>
				<image src="/static/icons/arrow-right.png" class="arrow-icon"></image>
			</view>
			<view class="option-item">
				<image src="/static/icons/favorite.png" class="option-icon"></image>
				<text class="option-text">我的收藏</text>
				<image src="/static/icons/arrow-right.png" class="arrow-icon"></image>
			</view>
			<view class="option-item">
				<image src="/static/icons/history.png" class="option-icon"></image>
				<text class="option-text">浏览历史</text>
				<image src="/static/icons/arrow-right.png" class="arrow-icon"></image>
			</view>
			<view class="option-item">
				<image src="/static/icons/feedback.png" class="option-icon"></image>
				<text class="option-text">意见反馈</text>
				<image src="/static/icons/arrow-right.png" class="arrow-icon"></image>
			</view>
			<view class="option-item">
				<image src="/static/icons/about.png" class="option-icon"></image>
				<text class="option-text">关于我们</text>
				<image src="/static/icons/arrow-right.png" class="arrow-icon"></image>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.container {
		min-height: 100vh;
		background-color: #f5f5f5;
		padding-bottom: 20rpx;
	}
	
	/* 用户信息样式 */
	.user-info {
		display: flex;
		align-items: center;
		padding: 40rpx 30rpx;
		background-color: #ffffff;
	}
	
	.avatar-container {
		margin-right: 30rpx;
	}
	
	.avatar {
		width: 120rpx;
		height: 120rpx;
		border-radius: 50%;
		background-color: #f0f0f0;
	}
	
	.user-details {
		flex: 1;
	}
	
	.username {
		font-size: 36rpx;
		font-weight: 500;
		margin-bottom: 10rpx;
		display: block;
	}
	
	.user-id {
		font-size: 26rpx;
		color: #999;
	}
	
	.settings-icon {
		width: 48rpx;
		height: 48rpx;
	}
	
	/* 数据统计样式 */
	.stats {
		display: flex;
		background-color: #ffffff;
		margin-top: 20rpx;
		padding: 30rpx 0;
	}
	
	.stat-item {
		flex: 1;
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	
	.stat-number {
		font-size: 36rpx;
		font-weight: 500;
		margin-bottom: 10rpx;
	}
	
	.stat-label {
		font-size: 26rpx;
		color: #666;
	}
	
	/* 选项列表样式 */
	.options-list {
		margin-top: 20rpx;
		background-color: #ffffff;
	}
	
	.option-item {
		display: flex;
		align-items: center;
		padding: 30rpx;
		border-bottom: 1rpx solid #f0f0f0;
	}
	
	.option-icon {
		width: 40rpx;
		height: 40rpx;
		margin-right: 20rpx;
	}
	
	.option-text {
		flex: 1;
		font-size: 30rpx;
	}
	
	.arrow-icon {
		width: 32rpx;
		height: 32rpx;
		opacity: 0.5;
	}
</style> 