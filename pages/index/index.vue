<template>
	<view class="home">
		<header>
			<swiper class="swiper" :previous-margin="25" :next-margin="20" :autoplay="true">
				<swiper-item><image src="../../static/img/home_swiper.png" mode=""></image></swiper-item>
				<swiper-item><image src="../../static/img/home_swiper.png" mode=""></image></swiper-item>
				<swiper-item><image src="../../static/img/home_swiper.png" mode=""></image></swiper-item>
				<swiper-item><image src="../../static/img/home_swiper.png" mode=""></image></swiper-item>
				<swiper-item><image src="../../static/img/home_swiper.png" mode=""></image></swiper-item>
			</swiper>
		</header>
		<main>
			<!-- 导航 -->
			<view class="nav">
				<view class="list">
					<image src="../../static/img/home_nav1.png" mode=""></image>
					<view>数学</view>
				</view>
				<view class="list">
					<image src="../../static/img/home_nav2.png" mode=""></image>
					<view>英语</view>
				</view>
				<view class="list">
					<image src="../../static/img/home_nav3.png" mode=""></image>
					<view>科学</view>
				</view>
				<view class="list">
					<image src="../../static/img/home_nav4.png" mode=""></image>
					<view>美术</view>
				</view>
				<view class="list">
					<image src="../../static/img/home_nav5.png" mode=""></image>
					<view>音乐</view>
				</view>
			</view>
			<!-- 测评 咨询 -->
			<view class="consult">
				<view class="left">
					<view class="consult-Leftimg"><image src="../../static/img/home_consult1.png" mode=""></image></view>
					<view>
						<view class="name">智能测评</view>
						<view>Reowingcommunity</view>
					</view>
				</view>
				<view class="right">
					<view class="consult-Leftimg"><image src="../../static/img/home_consult2.png" mode=""></image></view>
					<view>
						<view class="name">智能测评</view>
						<view>Expertconsultation</view>
					</view>
				</view>
			</view>
			<!-- 热门课程 -->
			<view class="course">
				<view class="tltie">
					<view>热门课程</view>
					<view>更多 ></view>
				</view>
				<swiper class="swiper" :previous-margin="0" :next-margin="100" :autoplay="true">
					<swiper-item><image src="../../static/img/home_swiper.png" mode=""></image></swiper-item>
					<swiper-item><image src="../../static/img/home_swiper.png" mode=""></image></swiper-item>
					<swiper-item><image src="../../static/img/home_swiper.png" mode=""></image></swiper-item>
					<swiper-item><image src="../../static/img/home_swiper.png" mode=""></image></swiper-item>
					<swiper-item><image src="../../static/img/home_swiper.png" mode=""></image></swiper-item>
				</swiper>
			</view>
		</main>
		<footer></footer>
	</view>
</template>
<script>
export default {
	data() {
		return {};
	},
	onLoad() {},
	methods: {}
};
</script>

<style lang="scss">
header {
	.swiper {
		width: 100%;
		height: 300rpx;
	}
	image {
		width: 96%;
		height: 100%;
		border-radius: 30rpx;
		background-image: 100% 100%;
	}
}
main {
	.nav {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 60rpx 50rpx;
		.list {
			text-align: center;
			color: #505050;
			font-size: 30rpx;
			image {
				width: 90rpx;
				height: 90rpx;
				background-size: 100% 100%;
			}
		}
	}
	.consult {
		display: flex;
		padding: 0 50rpx;
		.left {
			display: flex;
			align-items: center;
			justify-content: space-between;
			margin-right: 15rpx;
			padding: 0 20rpx;
			width: 100%;
			height: 180rpx;
			font-size: 20rpx;
			border-radius: 25rpx;
			background-color: #fff5e9;
			image {
				width: 80rpx;
				height: 85rpx;
				background-size: 100% 100%;
			}
			.name {
				text-align: center;
				font-size: 37rpx;
				color: #373833;
				font-weight: 700;
			}
		}
		.right {
			display: flex;
			align-items: center;
			justify-content: space-between;
			margin-left: 15rpx;
			width: 100%;
			height: 180rpx;
			padding: 0 20rpx;
			font-size: 20rpx;
			border-radius: 25rpx;
			background-color: #f3f8fe;
			image {
				width: 86rpx;
				height: 83rpx;
				background-size: 100% 100%;
			}
			.name {
				text-align: center;
				font-size: 37rpx;
				color: #373833;
				font-weight: 700;
			}
		}
	}
	.course {
		.tltie {
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding: 40rpx 50rpx;
			:nth-child(1) {
				font-size: 40rpx;
				font-weight: 600;
			}
			:nth-child(2) {
				font-size: 30rpx;
				color: #10c179;
			}
		}
		.swiper {
			padding-left: 50rpx;
			width: 100%;
			height: 300rpx;
		}
		image {
			width: 96%;
			height: 100%;
			border-radius: 30rpx;
			background-image: 100% 100%;
		}
	}
}
</style>
