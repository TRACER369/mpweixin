<template>
	<view class="container">
		<!-- 顶部标题区域 -->
		<view class="header">
			<view class="title">青英辅学</view>
			<view class="subtitle">高校知识付费领域整合营销平台</view>
		</view>

		<!-- 轮播图区域 -->
		<swiper class="swiper" circular autoplay interval="3000">
			<swiper-item>
				<view class="swiper-item">
					<view class="notice">
						<text class="notice-icon">🔊</text>
						<text class="notice-text">2025.4.10 [003] 中南大学生命科学学院招募...</text>
					</view>
				</view>
			</swiper-item>
		</swiper>

		<!-- 四个主要功能按钮 -->
		<view class="grid-section">
			<view class="grid">
				<view class="grid-item" v-for="(item, index) in mainFunctions" :key="index" @tap="navigateToFunction(item.path)">
					<image :src="item.icon" mode="aspectFit" class="grid-icon"></image>
					<text class="grid-text">{{item.name}}</text>
				</view>
			</view>
		</view>

		<!-- 底部服务卡片 -->
		<view class="service-section">
			<view class="service-row">
				<view class="service-card" @tap="navigateToService('recruitment')">
					<image src="/static/images/recruitment.png" mode="aspectFit" class="service-icon"></image>
					<text class="service-title">招商代理</text>
				</view>
				<view class="service-card" @tap="navigateToService('technical')">
					<image src="/static/images/technical.png" mode="aspectFit" class="service-icon"></image>
					<text class="service-title">技术服务</text>
				</view>
			</view>
			<view class="service-row">
				<view class="service-card" @tap="navigateToService('information')">
					<image src="/static/images/information.png" mode="aspectFit" class="service-icon"></image>
					<text class="service-title">信息咨询</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				mainFunctions: [
					{ name: '项目申请指导', icon: '/static/images/project.png', path: '/pages/project/index' },
					{ name: '竞赛指导', icon: '/static/images/competition.png', path: '/pages/competition/index' },
					{ name: '学业指导', icon: '/static/images/study.png', path: '/pages/study/index' },
					{ name: '升学指导', icon: '/static/images/education.png', path: '/pages/education/index' }
				]
			}
		},
		onLoad() {

		},
		methods: {
			navigateToFunction(path) {
				uni.navigateTo({
					url: path
				})
			},
			navigateToService(type) {
				uni.navigateTo({
					url: `/pages/service/${type}`
				})
			}
		}
	}
</script>

<style>
	.container {
		padding: 20rpx;
	}

	.header {
		text-align: center;
		padding: 20rpx 0;
	}

	.title {
		font-size: 40rpx;
		font-weight: bold;
	}

	.subtitle {
		font-size: 24rpx;
		color: #666;
		margin-top: 10rpx;
	}

	.swiper {
		height: 80rpx;
		background-color: #FFF5F5;
		border-radius: 10rpx;
		margin: 20rpx 0;
	}

	.swiper-item {
		display: flex;
		align-items: center;
		padding: 0 20rpx;
	}

	.notice {
		display: flex;
		align-items: center;
	}

	.notice-icon {
		margin-right: 10rpx;
	}

	.notice-text {
		font-size: 26rpx;
		color: #333;
	}

	.grid-section {
		margin: 30rpx 0;
	}

	.grid {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
	}

	.grid-item {
		width: 25%;
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: 20rpx 0;
	}

	.grid-icon {
		width: 80rpx;
		height: 80rpx;
		margin-bottom: 10rpx;
	}

	.grid-text {
		font-size: 24rpx;
		color: #333;
	}

	.service-section {
		margin-top: 30rpx;
	}

	.service-row {
		display: flex;
		justify-content: space-between;
		margin-bottom: 20rpx;
	}

	.service-card {
		background: #fff;
		border-radius: 20rpx;
		padding: 30rpx;
		width: 45%;
		box-shadow: 0 2rpx 10rpx rgba(0,0,0,0.1);
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.service-icon {
		width: 100rpx;
		height: 100rpx;
		margin-bottom: 20rpx;
	}

	.service-title {
		font-size: 28rpx;
		color: #333;
	}
</style>
