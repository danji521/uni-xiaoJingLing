<template>
	<view class="find">
		<header><tabControl :current="current" :values="items" bgc="#fff" :fixed="true" :scrollFlag="true" :isEqually="true" @clickItem="onClickItem"></tabControl></header>
		<main>
			<swiper class="swiper" style="height: 100%;" @change="scollSwiper" :current="current">
				<!-- 发现 -->
				<swiper-item class="titleFind">
					<scroll-view scroll-y="true" style="height: 100%;">
						<!-- 学习之路 -->
						<view class="nav"><image src="../../static/img/find_nav1.png" mode=""></image></view>
						<!-- 订阅 -->
						<view class="subscribe">
							<view class="list">
								<image src="../../static/img/find_sub1.png" mode=""></image>
								<view class="list-center">
									<text>免费</text>
									3-6岁
								</view>
								<view class="list-footer"><view>订阅</view></view>
							</view>
							<view class="list">
								<image src="../../static/img/find_sub2.png" mode=""></image>
								<view class="list-center">
									<text>免费</text>
									3-6岁
								</view>
								<view class="list-footer"><view>订阅</view></view>
							</view>
							<view class="list">
								<image src="../../static/img/find_sub3.png" mode=""></image>
								<view class="list-center">
									<text>免费</text>
									3-6岁
								</view>
								<view class="list-footer"><view>订阅</view></view>
							</view>
						</view>
						<!-- 推荐 -->
						<view class="recommend">
							<view class="title">
								<view class="left">推荐绘本</view>
								<view class="right">更多 ></view>
							</view>
							<view class="box">
								<view><image src="../../static/img/find_book1.png" mode=""></image></view>
								<view><image src="../../static/img/find_book2.png" mode=""></image></view>
							</view>
						</view>
					</scroll-view>
				</swiper-item>
				<!-- 社区 -->
				<swiper-item class="community">
					<scroll-view scroll-y="true" style="height: 100%;">
						<view class="nav">
							<view class="left">
								<image src="../../static/img/find_com1.png" mode=""></image>
								<view class="news">
									<view>教育问答</view>
									<view>教育问题专家有答</view>
								</view>
							</view>
							<view class="right">
								<image src="../../static/img/find_com2.png" mode=""></image>
								<view class="news">
									<view>教育问答</view>
									<view>教育问题专家有答</view>
								</view>
							</view>
						</view>
						<!-- 用户 -->
						<view class="list" v-for="(items, index) in user" :key="index">
							<view class="listUp">
								<view><image src="../../static/logo.png" mode=""></image></view>
								<view class="listUp-right">
									<view class="listUp-right-name">
										<text>张洋洋</text>
										<text>+关注</text>
									</view>
									<view class="listUp-right-time">2016-11-14 15:30</view>
								</view>
							</view>
							<view class="title">
								<image src="../../static/img/find_12.png" mode=""></image>
								孩子多多大适合开始学习早教课程?
							</view>
							<view class="video"><image src="../../static/img/find_15.png" mode=""></image></view>
							<view class="listFooter">
								<view class="listFooter-left">#教育问答</view>
								<view class="listFooter-right">
									<view><image src="../../static/img/find_news1.png" mode="">1223</image></view>
									<view><image src="../../static/img/find_news2.png" mode="">1223</image></view>
								</view>
							</view>
						</view>
					</scroll-view>
				</swiper-item>
			</swiper>
		</main>
		<footer></footer>
	</view>
</template>

<script>
import tabControl from '@/components/tabControl-tag/tabControl-tag.vue';
export default {
	components: { tabControl },
	data() {
		return {
			items: ['发现', '社区'],
			current: 0,
			// 社区用户信息
			user: [0, 1, 2, 2]
		};
	},
	methods: {
		onClickItem(val) {
			this.current = val.currentIndex;
		},
		scollSwiper(e) {
			this.current = e.target.current;
		}
	}
};
</script>

<style lang="scss">
::-webkit-scrollbar {
	width: 0;
	height: 0;
	color: transparent;
}
header {
	position: sticky;
	top: 0;
	z-index: 3;
}
main {
	height: 100vh;
	padding: 100rpx 20rpx 0 20rpx;
}

main .titleFind {
	.nav {
		width: 100%;
		height: 228rpx;
		image {
			width: 100%;
			height: 228rpx;
			border-radius: 30rpx;
			background-size: 100% 100%;
		}
	}
	.subscribe {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 20rpx 0;
	}
	.subscribe .list {
		text-align: center;
		image {
			width: 230rpx;
			height: 300rpx;
			border-radius: 30rpx;
			background-size: 100% 100%;
		}
	}
	.subscribe .list-center {
		font-size: 30rpx;
		color: #acacac;
		text {
			color: #fd7b30;
		}
	}
	.list-footer {
		display: flex;
		justify-content: center;
		align-items: center;
		margin-top: 30rpx;
		font-size: 32rpx;
		view {
			display: flex;
			justify-content: center;
			align-items: center;
			width: 140rpx;
			height: 60rpx;
			color: #ffffff;
			border-radius: 38rpx;
			background-color: #2ec987;
		}
	}
	.recommend {
		border-top: 14rpx solid #f6f6f6;
	}
	.recommend .title {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding-top: 20rpx;
		.left {
			color: #282828;
			font-size: 40rpx;
			font-weight: 600;
		}
		.right {
			color: #64d39e;
			font-size: 35rpx;
		}
	}
	.recommend .box {
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin-top: 50rpx;
		padding-bottom: 20rpx;
		border-bottom: 8rpx solid #f6f6f6;
		image {
			width: 350rpx;
			height: 380rpx;
			border-radius: 30rpx;
			background-size: 100% 100%;
		}
	}
}
main .community {
	.nav {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding-bottom: 40rpx;
		image {
			margin-left: 20rpx;
			width: 80rpx;
			height: 78rpx;
			background-size: 100% 100%;
		}
		.news {
			padding-right: 25rpx;
			color: #a4aaa8;
			font-size: 25rpx;
		}
		.news :nth-child(1) {
			color: #161616;
			font-size: 35rpx;
		}
		.left {
			display: flex;
			justify-content: space-between;
			align-items: center;

			width: 340rpx;
			height: 160rpx;
			border-radius: 30rpx;
			background-color: #f0fffa;
		}
		.right {
			display: flex;
			justify-content: space-between;
			align-items: center;
			width: 340rpx;
			height: 160rpx;
			border-radius: 30rpx;
			background-color: #f1f8fe;
		}
	}
	.list {
		padding: 30rpx 20rpx;
		border-top: 8px solid #f6f6f6;
	}
	.list .listUp {
		display: flex;
		justify-content: space-between;
		align-items: center;
		image {
			width: 80rpx;
			height: 80rpx;
			border-radius: 50%;
		}
		.listUp-right {
			padding-left: 20rpx;
			width: 100%;
		}
		.listUp-right-name {
			display: flex;
			justify-content: space-between;
			align-items: center;
			:nth-child(1) {
				font-size: 33rpx;
				color: #616161;
			}
			:nth-child(2) {
				font-size: 33rpx;
				color: #87deb3;
			}
		}
		.listUp-right-time {
			color: #bfbfbf;
			font-size: 30rpx;
		}
	}
	.title {
		display: flex;
		align-items: center;
		padding: 20rpx 0;
		font-size: 35rpx;
		font-weight: 500;
		color: #101010;
		image {
			margin-right: 15rpx;
			width: 50rpx;
			height: 50rpx;
			background-size: 100% 100%;
		}
	}
	.video {
		padding: 20rpx 0;
		text-align: center;
		image {
			width: 685rpx;
			height: 350rpx;
			border-radius: 30rpxk;
			background-size: 100% 100%;
		}
	}
	.listFooter {
		display: flex;
		justify-content: space-between;
		align-items: center;
		image {
			width: 30rpx;
			height: 30rpx;
			background-size: 100% 100%;
		}
		.listFooter-left {
			font-size: 30rpx;
			color: #87deb3;
		}
		.listFooter-right {
			display: flex;
			align-items: center;
			font-size: 30rpx;
			color: #dbdbdb;
			view {
				display: flex;
				align-items: center;
			}
		}
	}
}
</style>
