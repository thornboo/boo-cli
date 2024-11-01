<route lang="json5" type="page">
{
	style: {
		navigationBarTitleText: '首页',
	},
}
</route>

<template>
	<view class="bg-white overflow-hidden pt-2 px-4">
		<wd-button class="m-2" @click="goto('demo')">demo</wd-button>
		<wd-button class="m-2" @click="goto('textAndCommentCombo')">正文和评论组合组件</wd-button>
	</view>
	<TabBar />
</template>

<script lang="ts" setup>
	import TabBar from '../../components/tabbar/tabbar.vue'

	function goto(params: string) {
		uni.navigateTo({
			url: `/pages-sub/${params}/${params}`,
		})
	}
</script>

<style lang="scss" scoped></style>
