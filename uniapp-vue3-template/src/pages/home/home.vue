<route lang="json5" type="page">
{
	style: {
		navigationBarTitleText: '首页',
	},
}
</route>

<template>
	<view class="bg-white overflow-hidden pt-2 px-4">
		<h3 style="margin-bottom: 10px">按钮组件</h3>
		<wd-button style="margin: 5px">主要按钮</wd-button>
		<wd-button style="margin: 5px" type="success">成功按钮</wd-button>
		<wd-button style="margin: 5px" type="info">信息按钮</wd-button>
		<wd-button style="margin: 5px" type="warning">警告按钮</wd-button>
		<wd-button style="margin: 5px" type="error">危险按钮</wd-button>
	</view>
	<TabBar />
</template>

<script lang="ts" setup>
	import TabBar from '../../components/tabbar/tabbar.vue'
</script>

<style lang="scss" scoped></style>
