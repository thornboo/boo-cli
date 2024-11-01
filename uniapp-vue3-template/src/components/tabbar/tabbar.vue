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
			<wd-tabbar-item icon="hall" name="hall" title="大厅"></wd-tabbar-item>
			<wd-tabbar-item icon="about" name="about" title="关于"></wd-tabbar-item>
			<wd-tabbar-item icon="mine" name="mine" title="我的"></wd-tabbar-item>
		</wd-tabbar>
	</view>
</template>

<script lang="ts" setup>
	// 根据 name 来匹配
	const tabBar = ref('home')

	// 切换 tabbar 方法
	function switchTabBar(params) {
		console.log(params)

		uni.switchTab({
			url: `/pages/${params}/${params}`,
			success: (success) => {
				console.log(success)
			},
			fail: (error) => {
				console.log(error)
			},
		})
	}
</script>

<style lang="scss" scoped></style>
