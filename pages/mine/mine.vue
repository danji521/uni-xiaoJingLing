<template>
	<view class="mine">
		<header><image src="../../static/img/mine_header.png" mode=""></image></header>
		<nav>
			<view class="left"><image src="../../static/logo.png" mode=""></image></view>
			<view class="right">
				<!-- 登录 -->
				<view v-if="name == ''" class="login">立即登录</view>
				<!-- 信息 -->
				<view v-else class="name">
					<text>心悦妈妈</text>
					学员小学二年级
				</view>
				<view><image src="../../static/img/return.png" mode="" class="return"></image></view>
			</view>
		</nav>
		<main>
			<!--订单 优惠券 积分  -->
			<view class="discount">
				<view>
					<image src="../../static/img/mine_nav1.png" mode=""></image>
					<view>我的订单</view>
				</view>
				<view>
					<image src="../../static/img/mine_nav2.png" mode=""></image>
					<view>优惠券</view>
				</view>
				<view>
					<image src="../../static/img/mine_nav3.png" mode=""></image>
					<view>积分</view>
				</view>
			</view>
			<!-- 评价 关注 收藏  反馈  关于-->
			<view class="collect">
				<view class="list">
					<view>
						<image src="../../static/img/mine_main1.png" mode=""></image>
						我的评价
					</view>
					<view><image src="../../static/img/return.png" mode="" class="return"></image></view>
				</view>
				<view class="list">
					<view>
						<image src="../../static/img/mine_main2.png" mode=""></image>
						我的关注
					</view>
					<view><image src="../../static/img/return.png" mode="" class="return"></image></view>
				</view>
				<view class="list" style="margin-bottom:30rpx;">
					<view>
						<image src="../../static/img/mine_main3.png" mode=""></image>
						我的收藏
					</view>
					<view><image src="../../static/img/return.png" mode="" class="return"></image></view>
				</view>
				<view class="list">
					<view>
						<image src="../../static/img/mine_main4.png" mode=""></image>
						帮助反馈
					</view>
					<view><image src="../../static/img/return.png" mode="" class="return"></image></view>
				</view>
				<view class="list">
					<view>
						<image src="../../static/img/mine_main5.png" mode=""></image>
						关于我们
					</view>
					<view><image src="../../static/img/return.png" mode="" class="return"></image></view>
				</view>
			</view>
		</main>
		<footer></footer>
	</view>
</template>

<script>
export default {
	data() {
		return {
			name: ''
		};
	}
};
</script>

<style lang="scss">
.mine {
	height: 100vh;
	background-color: #f5f5f5;
}
header,
header image {
	width: 100%;
	height: 250rpx;
}
nav {
	display: flex;
	align-items: center;
	justify-content: space-between;
	padding: 0 30rpx;
	background-color: #ffffff;
	image {
		width: 150rpx;
		height: 150rpx;
		border-radius: 50%;
		border: 8rpx solid #ffffff;
		background-size: 100% 100%;
	}
	.left image {
		position: relative;
		bottom: 60rpx;
	}
	.right {
		display: flex;
		justify-content: space-between;
		align-items: center;
		position: relative;
		bottom: 40rpx;
		padding-left: 20rpx;
		width: 100%;
		color: #a2a2a2;
	}
	.return {
		width: 15rpx;
		height: 40rpx;
		background-image: 100% 100%;
	}
	.login {
		font-size: 39rpx;
		color: #08bc72;
	}
	.name {
		font-size: 30rpx;
		color: #5c5c5c;
		text {
			margin-right: 20rpx;
			font-size: 40rpx;
			color: #141414;
		}
	}
}
main {
	.discount {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 0 50rpx 30rpx 50rpx;
		margin-bottom: 30rpx;
		background-color: #ffffff;
		color: #252525;
		font-size: 35rpx;
		view {
			text-align: center;
		}
		image {
			width: 140rpx;
			height: 98rpx;
			background-size: 100% 100%;
		}
	}
	.collect {
		.list {
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding: 40rpx 30rpx;
			color: #121212;
			background-color: #ffffff;
			border-bottom: 1px solid #fbfbfb;
		}
		.list image {
			width: 107rpx;
			height: 50rpx;
			background-size: 100% 100%;
		}
		.list view {
			display: flex;
			justify-content: center;
			align-items: center;
			.return {
				width: 15rpx;
				height: 50rpx;
				background-image: 100% 100%;
			}
		}
	}
}
</style>
