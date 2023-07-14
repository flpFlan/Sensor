<template>
	<uni-search-bar class="top-bar" placeholder="请输入想要查找的内容" cancel-button="always" @cancel="back" />
</template>

<script setup>
	function back() {
		uni.navigateBack({
			delta: 1
		})
	}
</script>

<style scoped>
	.top-bar {
		margin-top: var(--status-bar-height);
	}
</style>