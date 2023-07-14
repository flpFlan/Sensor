<template>
	<view class="chat-send">
		<uni-easyinput type="text" class="chat-input" v-model="val" /><button :disabled="val==''"
			@click="send">发送</button>
	</view>
</template>

<script setup>
	import {
		ref,
		defineEmits
	} from 'vue'
	const emit = defineEmits(["onSend"])
	const val = ref('')

	function send() {
		emit("onSend", val.value);
		val.value = ''
	}
</script>

<style scoped>
	.chat-send {
		display: flex;
		position: fixed;
		align-items: flex-start;
		bottom: calc(var(--window-bottom)-10px);
		left: 0;
		right: 0;
		background: #ffffff;
		height: 100px;
	}

	.chat-input {
		flex: 1;
	}
	button{
		background-color:#9fefef;
		color: #ffffff;
	}
</style>