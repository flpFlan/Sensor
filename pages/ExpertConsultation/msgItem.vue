<template>
	<uni-card class="msg">
		<text>{{msg}}</text>
	</uni-card>
</template>

<script setup>
	import {defineProps} from 'vue'
	const props=defineProps(["msg"])
</script>

<style scoped>
	.msg{
		background-color: pink;
	}
</style>