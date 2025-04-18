<template>
	<view class="container">
		<!-- Header with back button, title and more options -->
		<view class="header">
			<view class="header-left">
				<image src="/static/icons/back.png" class="back-icon" @click="goBack"></image>
			</view>
			<view class="header-title">青英大学老师</view>
			<view class="header-right">
				<image src="/static/icons/more.png" class="more-icon"></image>
				<image src="/static/icons/camera.png" class="camera-icon"></image>
			</view>
		</view>
		
		<!-- Search bar -->
		<view class="search-container">
			<view class="search-box">
				<image src="/static/icons/search.png" class="search-icon"></image>
				<input type="text" placeholder="论文指导/实验操作/竞赛辅导/软件教学" class="search-input" />
			</view>
			<text class="cancel-btn">取消</text>
		</view>
		
		<!-- Feature grid - top row -->
		<view class="feature-grid">
			<view class="feature-item">
				<view class="feature-icon-bg green">
					<image src="/static/icons/skills.png" class="feature-icon"></image>
				</view>
				<text class="feature-text">技能提升</text>
			</view>
			<view class="feature-item">
				<view class="feature-icon-bg blue">
					<image src="/static/icons/academic.png" class="feature-icon"></image>
				</view>
				<text class="feature-text">学业指导</text>
			</view>
			<view class="feature-item">
				<view class="feature-icon-bg yellow">
					<image src="/static/icons/recommendation.png" class="feature-icon"></image>
				</view>
				<text class="feature-text">精准推荐</text>
			</view>
		</view>
		
		<!-- Feature grid - bottom row -->
		<view class="feature-grid">
			<view class="feature-item">
				<view class="feature-icon-bg blue-light">
					<image src="/static/icons/project.png" class="feature-icon"></image>
				</view>
				<text class="feature-text">查项目</text>
			</view>
			<view class="feature-item">
				<view class="feature-icon-bg pink">
					<image src="/static/icons/mentor.png" class="feature-icon"></image>
				</view>
				<text class="feature-text">查导师</text>
			</view>
			<view class="feature-item">
				<view class="feature-icon-bg green-light">
					<image src="/static/icons/expert.png" class="feature-icon"></image>
				</view>
				<text class="feature-text">找专家</text>
			</view>
		</view>
		
		<!-- Hot areas section -->
		<view class="hot-areas">
			<view class="section-header">
				<text class="section-title">热门领域</text>
				<view class="view-all">
					<text>全部</text>
					<image src="/static/icons/arrow-right.png" class="arrow-icon"></image>
				</view>
			</view>
			
			<!-- Hot areas grid -->
			<view class="hot-areas-grid">
				<view class="hot-area-item" v-for="(item, index) in hotAreas" :key="index">
					<image :src="item.icon" class="hot-area-icon"></image>
					<text class="hot-area-text">{{item.text}}</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				hotAreas: [
					{ icon: '/static/icons/computer.png', text: '计算机科学' },
					{ icon: '/static/icons/biology.png', text: '生物技术' },
					{ icon: '/static/icons/law.png', text: '法学' },
					{ icon: '/static/icons/medicine.png', text: '医学' },
					{ icon: '/static/icons/finance.png', text: '金融商科' },
					{ icon: '/static/icons/education.png', text: '教育学' },
					{ icon: '/static/icons/electronics.png', text: '电子信息' },
					{ icon: '/static/icons/media.png', text: '新闻传播' },
					{ icon: '/static/icons/environment.png', text: '环境科学' },
					{ icon: '/static/icons/mechanical.png', text: '机械工程' },
					{ icon: '/static/icons/art.png', text: '艺术设计' },
					{ icon: '/static/icons/ai.png', text: '人工智能' }
				]
			}
		},
		methods: {
			goBack() {
				uni.navigateBack();
			}
		}
	}
</script>

<style>
	.container {
		background-color: #f5f5f5;
		min-height: 100vh;
		padding-bottom: 20rpx;
	}
	
	/* Header styles */
	.header {
		display: flex;
		align-items: center;
		justify-content: space-between;
		height: 88rpx;
		padding: 20rpx;
		background-color: #fff;
		position: relative;
		padding-top: 50rpx;
	}
	
	.header-left, .header-right {
		display: flex;
		align-items: center;
	}
	
	.header-title {
		font-size: 36rpx;
		font-weight: bold;
		text-align: center;
		flex: 1;
	}
	
	.back-icon, .more-icon, .camera-icon {
		width: 48rpx;
		height: 48rpx;
		margin: 0 10rpx;
	}
	
	/* Search bar styles */
	.search-container {
		display: flex;
		align-items: center;
		padding: 20rpx;
		background-color: #fff;
	}
	
	.search-box {
		display: flex;
		align-items: center;
		background-color: #f5f5f5;
		border-radius: 36rpx;
		padding: 0 20rpx;
		height: 72rpx;
		flex: 1;
	}
	
	.search-icon {
		width: 40rpx;
		height: 40rpx;
		margin-right: 10rpx;
	}
	
	.search-input {
		flex: 1;
		height: 72rpx;
		font-size: 28rpx;
	}
	
	.cancel-btn {
		padding: 0 20rpx;
		font-size: 30rpx;
		color: #333;
	}
	
	/* Feature grid styles */
	.feature-grid {
		display: flex;
		justify-content: space-around;
		padding: 20rpx;
		background-color: #fff;
		margin-top: 2rpx;
	}
	
	.feature-item {
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 33.33%;
	}
	
	.feature-icon-bg {
		width: 120rpx;
		height: 120rpx;
		border-radius: 50%;
		display: flex;
		justify-content: center;
		align-items: center;
		margin-bottom: 15rpx;
	}
	
	.green {
		background-color: #4CD964;
	}
	
	.blue {
		background-color: #1CB5FF;
	}
	
	.yellow {
		background-color: #FFCC33;
	}
	
	.blue-light {
		background-color: #007AFF;
	}
	
	.pink {
		background-color: #FF2D55;
	}
	
	.green-light {
		background-color: #5AC8FA;
	}
	
	.feature-icon {
		width: 60rpx;
		height: 60rpx;
	}
	
	.feature-text {
		font-size: 26rpx;
		color: #333;
	}
	
	/* Hot areas section */
	.hot-areas {
		margin-top: 20rpx;
		background-color: #fff;
		padding: 20rpx;
	}
	
	.section-header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin-bottom: 20rpx;
	}
	
	.section-title {
		font-size: 32rpx;
		font-weight: bold;
		color: #333;
	}
	
	.view-all {
		display: flex;
		align-items: center;
		color: #999;
		font-size: 26rpx;
	}
	
	.arrow-icon {
		width: 24rpx;
		height: 24rpx;
		margin-left: 5rpx;
	}
	
	/* Hot areas grid */
	.hot-areas-grid {
		display: flex;
		flex-wrap: wrap;
	}
	
	.hot-area-item {
		width: 25%;
		display: flex;
		flex-direction: column;
		align-items: center;
		margin-bottom: 30rpx;
	}
	
	.hot-area-icon {
		width: 80rpx;
		height: 80rpx;
		margin-bottom: 10rpx;
	}
	
	.hot-area-text {
		font-size: 24rpx;
		color: #333;
		text-align: center;
	}
</style> 