<template>
	<view class="container">
		<!-- 顶部状态栏 -->
		<view class="status-bar">
			<view class="left-dot">•</view>
			<text class="carrier">•••••  中国移动</text>
			<text class="time">12:00</text>
			<text class="battery">•</text>
		</view>
		
		<!-- 头部区域 -->
		<view class="header">
			<view class="header-content">
				<text class="title">我的</text>
			</view>
			<view class="header-icons">
				<text class="more-icon">•••</text>
				<text class="circle-icon">○</text>
			</view>
		</view>
		
		<!-- 用户信息 -->
		<view class="user-info">
			<view class="avatar">
				<text class="avatar-text">用户</text>
			</view>
			<view class="user-details">
				<text class="user-name">未登录</text>
				<text class="user-desc">点击登录账号</text>
			</view>
			<view class="arrow">></view>
		</view>
		
		<!-- 菜单列表 -->
		<view class="menu-list">
			<view class="menu-item">
				<view class="menu-icon blue">
					<text class="icon-text">订</text>
				</view>
				<text class="menu-text">我的订单</text>
				<view class="arrow">></view>
			</view>
			
			<view class="menu-item">
				<view class="menu-icon green">
					<text class="icon-text">课</text>
				</view>
				<text class="menu-text">我的课程</text>
				<view class="arrow">></view>
			</view>
			
			<view class="menu-item">
				<view class="menu-icon orange">
					<text class="icon-text">收</text>
				</view>
				<text class="menu-text">我的收藏</text>
				<view class="arrow">></view>
			</view>
			
			<view class="menu-item">
				<view class="menu-icon purple">
					<text class="icon-text">设</text>
				</view>
				<text class="menu-text">设置</text>
				<view class="arrow">></view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '我的'
			}
		},
		onLoad() {
			// 页面加载逻辑
		},
		methods: {
			// 方法定义
		}
	}
</script>

<style>
	.container {
		padding: 0;
		background-color: #f5f5f5;
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
		min-height: 100vh;
	}
	
	/* 状态栏样式 */
	.status-bar {
		position: relative;
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 8rpx 20rpx;
		background-color: #fff;
		height: 44rpx;
		font-size: 24rpx;
		color: #000;
	}
	
	.left-dot {
		font-size: 30rpx;
	}
	
	.carrier {
		position: absolute;
		left: 80rpx;
		font-size: 24rpx;
	}
	
	.time {
		position: absolute;
		left: 50%;
		transform: translateX(-50%);
		font-weight: 500;
	}
	
	.battery {
		position: absolute;
		right: 20rpx;
		font-size: 40rpx;
	}
	
	/* 头部区域样式 */
	.header {
		display: flex;
		justify-content: space-between;
		padding: 20rpx 30rpx;
		background-color: #fff;
		border-bottom: 2rpx solid #f0f0f0;
	}
	
	.header-content {
		display: flex;
		flex-direction: column;
	}
	
	.title {
		font-size: 36rpx;
		font-weight: bold;
	}
	
	.header-icons {
		display: flex;
		align-items: center;
	}
	
	.more-icon {
		margin-right: 20rpx;
		font-size: 24rpx;
		color: #999;
	}
	
	.circle-icon {
		font-size: 40rpx;
		color: #333;
	}
	
	/* 用户信息区域 */
	.user-info {
		display: flex;
		align-items: center;
		background-color: #fff;
		margin: 20rpx;
		padding: 30rpx;
		border-radius: 16rpx;
		position: relative;
	}
	
	.avatar {
		width: 120rpx;
		height: 120rpx;
		border-radius: 50%;
		background-color: #e0e0e0;
		display: flex;
		justify-content: center;
		align-items: center;
		margin-right: 30rpx;
	}
	
	.avatar-text {
		color: #999;
		font-size: 32rpx;
	}
	
	.user-details {
		flex: 1;
	}
	
	.user-name {
		font-size: 32rpx;
		font-weight: bold;
		margin-bottom: 10rpx;
	}
	
	.user-desc {
		font-size: 26rpx;
		color: #999;
	}
	
	.arrow {
		color: #ccc;
		font-size: 32rpx;
	}
	
	/* 菜单列表 */
	.menu-list {
		background-color: #fff;
		margin: 20rpx;
		border-radius: 16rpx;
		overflow: hidden;
	}
	
	.menu-item {
		display: flex;
		align-items: center;
		padding: 30rpx;
		border-bottom: 1rpx solid #f0f0f0;
	}
	
	.menu-item:last-child {
		border-bottom: none;
	}
	
	.menu-icon {
		width: 60rpx;
		height: 60rpx;
		border-radius: 10rpx;
		display: flex;
		justify-content: center;
		align-items: center;
		margin-right: 30rpx;
	}
	
	.icon-text {
		color: #fff;
		font-size: 28rpx;
	}
	
	.blue {
		background-color: #3498db;
	}
	
	.green {
		background-color: #2ecc71;
	}
	
	.orange {
		background-color: #f39c12;
	}
	
	.purple {
		background-color: #9b59b6;
	}
	
	.menu-text {
		flex: 1;
		font-size: 30rpx;
		color: #333;
	}
</style> 