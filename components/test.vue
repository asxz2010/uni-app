<template>
	<view id="myview">
		<view>test组件{{ title }}</view>
		<button @click="sendTo">给父组件传值</button>
	</view>
</template>

<script>
	export default {
		data(){
			return {
				num: 3,
				timeMachine: null,
			}
		},
		methods: {
			sendTo(){
				console.log(1111111111)
				this.$emit('getNum', this.num)
				console.log(22222222)
			}
		},
		props: ['title'],
		beforeCreate(){
			console.log('实例开始实例化', this.num)
		},
		created(){
			// console.log('created', this.num)
			// this.timeMachine = setInterval(()=>{
			// 	console.log('定时器执行中')
			// }, 1200)
		},
		beforeMount(){
			console.log('beforeMount', document.getElementById('myview'))
		},
		mounted(){
			console.log('mounted', document.getElementById('myview'))
		},
		destroyed(){
			clearInterval(this.timeMachine)
		}
	}
	
</script>

<style>
</style>
