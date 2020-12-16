<template>
	<view>
		<view>导航页</view>
		
		<!-- 声明式导航 -->
		<navigator url="/pages/detail/detail?id=8&age=20">跳转到详情页</navigator>
		<navigator url="/pages/message/message" open-type="switchTab">跳转到信息页</navigator>
		<!-- redirect 关闭当前页，跳转到目标页 -->
		<navigator url="/pages/detail/detail" open-type="redirect">跳转到详情页</navigator>
		
		<!-- 编程式导航 -->
		<button @click="toDetail">跳转到详情页</button>
		<button @click="toMessage">跳转到信息页</button>
		<button type="primary" @click="toMessage2">跳转到详情面并关闭当前页面</button>
	</view>
</template>

<script>
	export default {
		methods:{
			toDetail(){
				uni.navigateTo({
					url: '/pages/detail/detail?id=10&age=20'
				})
			},
			
			toMessage(){
				uni.switchTab({
					url: '/pages/message/message'
				})
			},
			
			toMessage2(){
				uni.redirectTo({
					url: '/pages/detail/detail'
				})
			}
			
		},
		onUnload() {
			console.log('导航页面卸载了')
		}
	}
	
</script>

<style>
</style>
