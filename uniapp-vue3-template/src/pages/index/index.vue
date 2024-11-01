<!-- 使用 type="home" 将属性设置首页，其他页面不需要设置，默认为page；推荐使用json5，更强大且允许注释 -->
<route lang="json5" type="home">
{
	style: {
		navigationStyle: 'custom',
		navigationBarTitleText: '启动页',
	},
}
</route>

<template>
	<view class="container">
		<wd-img :src="indexPageImage" class="back-image">
			<template #loading>
				<view class="loading-style-index">
					<wd-loading />
				</view>
			</template>
			<template #error>
				<wd-img :src="indexLoadingError" class="back-error" />
			</template>
		</wd-img>
	</view>
</template>

<script lang="ts" setup>
	// 注意微信小程序 image 标签路径接受二进制数据以及 base64 编码，单独使用 import 图片路径无法访问
	// import { joy } from '../images/joy'
	const homePageImage = 'data:image/jpeg;base64,...' // 图片文件base64
	const indexPageImage = '../../static/images/index.png'
	const indexLoadingError = '../../static/images/error.png'

	// 延迟3秒跳转到首页
	setTimeout(() => {
		uni.reLaunch({
			url: '/pages/home/home',
		})
	}, 3000)
</script>

<style lang="scss" scoped>
	page {
		height: 100%;
	}

	.container {
		display: flex;
		width: 100%;
		height: 100%;
	}

	.loading-style-index {
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.back-image {
		width: 100%;
		height: 100vh; // vh表示视口高度的百分比
	}

	.back-error {
		width: 100%;
		height: 50vh;
		object-fit: cover;
	}
</style>
