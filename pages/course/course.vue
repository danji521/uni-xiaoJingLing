<template>
	<view class="course">
		<header>
			<view>
				<image src="../../static/img/course_nav1.png" mode=""></image>
				<view>课表</view>
			</view>
			<view>
				<image src="../../static/img/course_nav2.png" mode=""></image>
				<view>下载</view>
			</view>
			<view>
				<image src="../../static/img/course_nav3.png" mode=""></image>
				<view>记录</view>
			</view>
			<view>
				<image src="../../static/img/course_nav4.png" mode=""></image>
				<view>已购</view>
			</view>
		</header>
		<main>
			<!-- 老师课程 -->
			<view class="list" v-for="(item, index) in course" :key="index">
				<view class="tltie">夏恩少儿英语</view>
				<view class="news">共96节 | 第3节 | 3月18日 20:00 开课</view>
				<view class="teacher">
					<view class="teacherLeft">
						<image src="../../static/logo.png" mode=""></image>
						<view class="teacherLeft-name">
							<view class="name">赵老师</view>
							<view>主讲</view>
						</view>
					</view>
					<view class="teacherRight">学习</view>
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
			// 课程
			course: [1, 2, 3, 3,4,5,6,7]
		};
	}
};
</script>

<style lang="scss">
.course {
	height: 100vh;
	background-color: #ffffff;
}
header {
	display: flex;
	justify-content: space-between;
	align-items: center;
	position:sticky;
	top: 0;
	padding: 20rpx 60rpx;
	color: #7b7b7b;
	font-size: 30rpx;
	background-color: #ffffff;
	z-index: 2;
	image {
		width: 90rpx;
		height: 70rpx;
		background-size: 100% 100%;
	}
	view {
		text-align: center;
	}
}
main {
	padding: 0 30rpx;
	.list {
		padding:10rpx 30rpx;
		margin-bottom: 30rpx;
		border-radius: 30rpx;
		background-color: #94d361;
		color: #ffffff;
		.tltie {
			font-size: 35rpx;
		}
		.news {
			font-size: 25rpx;
			color: #fff9ff;
		}
		.teacher {
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding-top: 14rpx;
			font-size: 30rpx;
		}
		.teacherLeft {
			display: flex;
		}
		.teacherLeft .name {
			font-size: 35rpx;
			color: #fffdfb;
		}
		.teacherLeft image {
			margin-right: 20rpx;
			width: 90rpx;
			height: 90rpx;
			border-radius: 50%;
			border: 2px solid #ffffff;
			background-size: 100% 100%;
		}
		.teacherLeft-name {
			padding-top: 10rpx;
		}
		.teacherRight {
			display: flex;
			justify-content: center;
			align-items: center;
			position: relative;
			top: 8rpx;
			color: #01bd69;
			border-radius: 25rpx;
			background-color: #ffffff;
			width: 130rpx;
			height: 60rpx;
			font-size: 30rpx;
		}
	}
}
</style>
