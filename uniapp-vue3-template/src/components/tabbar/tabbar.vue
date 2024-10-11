<template>
	<view>
		<wd-tabbar
			v-model="tabBar"
			fixed
			placeholder
			safeAreaInsetBottom
			@change="switchTabBar(tabBar)"
		>
			<wd-tabbar-item icon="home" name="home" title="首页"></wd-tabbar-item>
			<wd-tabbar-item icon="cart" name="cart" title="分类"></wd-tabbar-item>
			<wd-tabbar-item icon="setting" name="setting" title="设置"></wd-tabbar-item>
			<wd-tabbar-item icon="user" name="user" title="我的"></wd-tabbar-item>
		</wd-tabbar>
	</view>
</template>

<script lang="ts" setup>
	const tabBar = ref('home')

	function switchTabBar(params) {
		console.log(params)
		uni.switchTab({
			url: 'pages/index/index',
			success: () => {
				console.log('switchTab Success')
			},
		})
	}
</script>

<style lang="scss" scoped></style>
