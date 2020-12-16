<template>
	<view>
		a组件：<button @click="changeB">修改b组件的数据</button>
	</view>
</template>

<script>
	export default {
		data(){
			return {
				num: 3
			}
		},
		methods: {
			changeB(){
				uni.$emit('updateNum', this.num)
			}
		}
	}
</script>

<style>
</style>
