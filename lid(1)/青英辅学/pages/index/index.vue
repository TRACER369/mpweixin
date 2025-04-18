<template>
	<view class="container">
		<!-- 顶部状态栏 -->
		<view class="status-bar">
			<text class="carrier">••••• 中国移动</text>
			<text class="time">12:00</text>
			<text class="battery">•</text>
		</view>
		
		<!-- 头部区域 -->
		<view class="header">
			<view class="header-content">
				<text class="title">首页</text>
				<view class="app-info">
					<text class="app-name">青英辅学</text>
					<text class="app-desc">高校知识付费领域综合营销平台</text>
				</view>
			</view>
			<view class="header-icons">
				<text class="more-icon">•••</text>
				<text class="circle-icon">○</text>
			</view>
		</view>
		
		<!-- 付费产品区域 -->
		<view class="pay-section">
			<view class="pay-title">知识付费产品区</view>
			<view class="pay-items">
				<view class="pay-item">
					<view class="pay-icon medal">
						<text>○</text>
					</view>
					<text class="pay-text">付费课程</text>
				</view>
				<view class="pay-item">
					<view class="pay-icon qa">
						<text>三1</text>
					</view>
					<text class="pay-text">付费问答</text>
				</view>
				<view class="pay-item">
					<view class="pay-icon reward">
						<text>☀</text>
					</view>
					<text class="pay-text">付费打赏</text>
				</view>
			</view>
		</view>
		
		<!-- 公告栏 -->
		<view class="announcement">
			<text class="sound-icon">🔊</text>
			<text class="announcement-text">2025.4.10 [003] 中南大学生命科学学院招募一……</text>
		</view>
		
		<!-- 导航菜单 -->
		<view class="nav-menu">
			<view class="nav-item">
				<view class="nav-icon red">
					<text>🍎</text>
				</view>
				<view class="nav-text">
					<text>项目申</text>
					<text>请指导</text>
				</view>
			</view>
			<view class="nav-item">
				<view class="nav-icon blue">
					<text>🔧</text>
				</view>
				<view class="nav-text">
					<text>竞赛</text>
					<text>指导</text>
				</view>
			</view>
			<view class="nav-item">
				<view class="nav-icon pink">
					<text>🛡️</text>
				</view>
				<view class="nav-text">
					<text>学业</text>
					<text>指导</text>
				</view>
			</view>
			<view class="nav-item">
				<view class="nav-icon purple">
					<text>🛏️</text>
				</view>
				<view class="nav-text">
					<text>升学</text>
					<text>指导</text>
				</view>
			</view>
		</view>
		
		<!-- 热门产品标题 -->
		<view class="hot-products-title">
			<text>热门产品</text>
		</view>
		
		<!-- 热门产品 -->
		<view class="hot-products">
			<!-- 产品卡片 1 -->
			<view class="product-card">
				<view class="product-image cv">
					<text>CV</text>
				</view>
				<view class="product-info">
					<view class="product-title">CVer计算机视觉</view>
					<view class="product-stats">
						<text>Arxiui 创建 · 已更新 2570 天 · 19067 人已加入</text>
					</view>
					<view class="product-desc">
						<text>最大的计算机视觉AI知识星球！每日更新，第一时间分享最新前沿的计算机视觉、AIGC、深度学习、自动驾驶、医疗影像、遥感等领域的...</text>
					</view>
				</view>
				<view class="product-price">￥ 269</view>
			</view>
			
			<!-- 分隔线 -->
			<view class="divider"></view>
			
			<!-- 产品卡片 2 -->
			<view class="product-card">
				<view class="product-image java">
					<text>Java</text>
				</view>
				<view class="product-info">
					<view class="product-title">JavaGuide&Java面试文摘</view>
					<view class="product-stats">
						<text>Guide 创建 · 已更新 2090 天 · 36044 人已加入</text>
					</view>
					<view class="product-desc">
						<text>做最好的Java学习指南，2年8万+人已见证，C站开源书籍...</text>
					</view>
				</view>
				<view class="product-price">￥ 179</view>
			</view>
			
			<!-- 分隔线 -->
			<view class="divider"></view>
			
			<!-- 产品卡片 3 -->
			<view class="product-card">
				<view class="product-image code">
					<text>码农</text>
				</view>
				<view class="product-info">
					<view class="product-title">码农杂谈</view>
					<view class="product-stats">
						<text>小师哥 创建 · 已更新 2090 天 · 17722 人已加入</text>
					</view>
					<view class="product-desc">
						<text>进步学习，突破自我，提高核心能力，在 IT 领域破局...</text>
					</view>
				</view>
				<view class="product-price">￥ 159</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '青英辅学'
			}
		},
		onLoad() {
			console.log('Index page loaded')
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
		margin-bottom: 8rpx;
	}
	
	.app-info {
		display: flex;
		flex-direction: column;
	}
	
	.app-name {
		font-size: 36rpx;
		font-weight: bold;
	}
	
	.app-desc {
		font-size: 24rpx;
		color: #666;
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
	
	/* 付费产品区域样式 */
	.pay-section {
		background-color: #fff;
		margin: 20rpx 20rpx;
		padding: 30rpx 20rpx;
		border-radius: 16rpx;
		box-shadow: 0 2rpx 10rpx rgba(0,0,0,0.05);
	}
	
	.pay-title {
		font-size: 32rpx;
		font-weight: bold;
		text-align: center;
		margin-bottom: 30rpx;
	}
	
	.pay-items {
		display: flex;
		justify-content: space-around;
	}
	
	.pay-item {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	
	.pay-icon {
		width: 90rpx;
		height: 90rpx;
		border-radius: 50%;
		display: flex;
		justify-content: center;
		align-items: center;
		margin-bottom: 15rpx;
		font-size: 36rpx;
		color: #fff;
	}
	
	.medal {
		background-color: #ffd700;
	}
	
	.qa {
		background-color: #3498db;
	}
	
	.reward {
		background-color: #f39c12;
	}
	
	.pay-text {
		font-size: 28rpx;
		color: #333;
	}
	
	/* 公告栏样式 */
	.announcement {
		display: flex;
		align-items: center;
		background-color: #fff;
		padding: 15rpx 30rpx;
		margin: 0 20rpx 20rpx 20rpx;
		border-radius: 10rpx;
	}
	
	.sound-icon {
		margin-right: 20rpx;
		color: #6495ED;
	}
	
	.announcement-text {
		font-size: 26rpx;
		color: #6495ED;
	}
	
	/* 导航菜单样式 */
	.nav-menu {
		display: flex;
		justify-content: space-between;
		background-color: #fff;
		margin: 0 20rpx 20rpx 20rpx;
		padding: 30rpx;
		border-radius: 16rpx;
	}
	
	.nav-item {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	
	.nav-icon {
		width: 110rpx;
		height: 110rpx;
		border-radius: 50%;
		display: flex;
		justify-content: center;
		align-items: center;
		margin-bottom: 15rpx;
		font-size: 48rpx;
	}
	
	.red {
		background: linear-gradient(135deg, #ff7878, #ff3b3b);
	}
	
	.blue {
		background: linear-gradient(135deg, #78c5ff, #3b9eff);
	}
	
	.pink {
		background: linear-gradient(135deg, #ff78d2, #ff3bd1);
	}
	
	.purple {
		background: linear-gradient(135deg, #b278ff, #9a3bff);
	}
	
	.nav-text {
		font-size: 26rpx;
		text-align: center;
		line-height: 1.3;
		color: #333;
	}
	
	/* 热门产品标题 */
	.hot-products-title {
		font-size: 32rpx;
		font-weight: bold;
		padding: 30rpx 30rpx 15rpx 30rpx;
		background-color: #fff;
		margin: 0 20rpx;
		border-top-left-radius: 16rpx;
		border-top-right-radius: 16rpx;
	}
	
	/* 热门产品样式 */
	.hot-products {
		background-color: #fff;
		padding: 0 30rpx 30rpx 30rpx;
		margin: 0 20rpx 20rpx 20rpx;
		border-bottom-left-radius: 16rpx;
		border-bottom-right-radius: 16rpx;
	}
	
	.product-card {
		display: flex;
		position: relative;
		padding: 20rpx 0;
	}
	
	.divider {
		height: 1rpx;
		background-color: #f0f0f0;
		margin: 0;
	}
	
	.product-image {
		width: 100rpx;
		height: 100rpx;
		border-radius: 10rpx;
		margin-right: 20rpx;
		display: flex;
		justify-content: center;
		align-items: center;
		font-weight: bold;
		color: #fff;
		font-size: 24rpx;
	}
	
	.cv {
		background-color: #48a3ff;
	}
	
	.java {
		background-color: #ff4848;
		font-size: 20rpx;
	}
	
	.code {
		background-color: #ff8c48;
	}
	
	.product-info {
		flex: 1;
		padding-right: 50rpx;
	}
	
	.product-title {
		font-size: 28rpx;
		font-weight: bold;
		margin-bottom: 8rpx;
		color: #333;
	}
	
	.product-stats {
		font-size: 22rpx;
		color: #999;
		margin-bottom: 8rpx;
	}
	
	.product-desc {
		font-size: 22rpx;
		color: #999;
		line-height: 1.4;
	}
	
	.product-price {
		position: absolute;
		right: 0;
		top: 20rpx;
		font-size: 24rpx;
		color: #ff6b6b;
	}
</style>
