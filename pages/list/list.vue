<template>
	<view>
		<button @click="getApi">发送</button>
		<button type="primary" @click="setlocal">存储数据</button>
		<button type="primary" @click="getlocal">获取数据</button>
		<button type="primary" @click="removelocal">删除数据</button>
		<view>列表页</view>
		<view v-for="num in list" class="box">{{ num }}</view>
		<!-- <button @click="pointMe">点我</button> -->
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: ['11111', '22222', '33333', '44444', '55555', '11111', '22222', '33333', '44444', '55555']
			}
		},
		onPullDownRefresh() {
			console.log('触发了下拉刷新')
			setTimeout(() => {
				this.list = ['55555', '22222', '33333', '44444', '11111']
				uni.stopPullDownRefresh() 
			}, 2000)
		},
		onReachBottom() {
			console.log('页面触底了')
			this.list = [...this.list, ...['77777', '88888']]
		},
		methods: {
			pointMe() {
				uni.startPullDownRefresh()
			},

			getApi() {
				uni.request({
					url: 'http://localhost:8082/api/getlunbo',
					success(res) {
						console.log(res)
					}
				})
			},
			
			setlocal(){
				// uni.setStorage({
				// 	key: 'id',
				// 	data: '80',
				// 	success(res){
				// 		console.log('存储成功', res)
				// 	}
				// })
				uni.setStorageSync('id', '100')
			},
			
			getlocal(){
				// uni.getStorage({
				// 	key: 'id',
				// 	success(res){
				// 		console.log('获取成功', res.data)
				// 	}
				// })
				const id = uni.getStorageSync('id')
				console.log(id)
			},
			
			removelocal(){
				// uni.removeStorage({
				// 	key: 'id',
				// 	success(res){
				// 		console.log('删除成功', res)
				// 	}
				// })
				uni.removeStorageSync('id')
			}
		}
	}
</script>

<style>
	.box {
		width: 100px;
		height: 100px;
	}
</style>
