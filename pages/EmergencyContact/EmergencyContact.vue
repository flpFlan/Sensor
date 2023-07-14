<template>
	<uni-nav-bar class="top-bar" shadow fixed right-icon="search" @clickRight="search">
		<view class="title">应急联系</view>
	</uni-nav-bar>
</template>

<script setup>
	function search(){
		uni.navigateTo({ url: '/pages/Search/Search' })
	}
</script>

<style>
	.title{
		font-family: Georgia, 'Times New Roman', Times, serif;
		font-size: 25px;
		margin: 8px;
		margin-left: 25%;
		padding: 0;
	}
	.top-bar {
		margin-top: var(--status-bar-height);
	}
</style>