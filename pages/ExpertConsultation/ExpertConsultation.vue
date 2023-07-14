<template>
	<uni-nav-bar class="top-bar" shadow fixed right-icon="search" @clickRight="search">
		<view class="title">专家问诊</view>
	</uni-nav-bar>
	<view v-for="msg in msgList" :key="msg">
		<msg-item :msg="msg"></msg-item>
	</view>
	<input-form @onSend="onSend"/>
</template>

<script setup>
	import msgItem from './msgItem.vue'
	import inputForm from './inputForm.vue'
	import {ref} from 'vue'
	const msgList=ref(['你好'])
	function search(){
		uni.navigateTo({ url: '/pages/Search/Search' })
	}
	function onSend(msg){
		msgList.value.push(msg)
	}
</script>

<style scoped>
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