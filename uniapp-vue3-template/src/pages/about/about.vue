<route lang="json5" type="page">
{
	style: {
		navigationBarTitleText: '关于',
	},
}
</route>

<template>
	<view
		:style="{ marginTop: safeAreaInsets?.top + 'px' }"
		class="bg-white overflow-hidden pt-2 px-4"
	>
		<view class="text-center text-3xl mt-8">uniapp-vue3-template</view>
		<view class="mt-8 pl-2">
			<p>
				本项目是基于
				<a href="https://codercup.github.io/unibest-docs/">unibest</a>
				的base模版修改的，使其更加符合uniapp小程序开发，符合当前的业务逻辑。
			</p>
			<br />
			<span>
				其中组件库使用的是
				<a href="https://wot-design-uni.netlify.app/">Wot Design Uni</a>
			</span>
		</view>
	</view>
	<TabBar />
</template>

<script lang="ts" setup>
	import TabBar from '../../components/tabbar/tabbar.vue'
	// 获取屏幕边界到安全区域距离
	const { safeAreaInsets } = uni.getSystemInfoSync()
</script>

<style lang="scss" scoped></style>
