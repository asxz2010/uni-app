<template>
	<view>
		<image :src="imgUrl"></image>
		<view v-for="p in arr" :key="p.id">序号：{{ p.id }} 名字：{{ p.name }} 年龄：{{ p.age }}</view>
		<button @click="pointMe(20, $event)">点我</button>
	</view>
</template>

<script>
	export default {
		data(){
			return {
				imgUrl: 'https://scpic1.chinaz.net/Files/pic/pic9/202012/apic29431_s.jpg',
				arr: [
					{
						id: 1,
						name: '宋小宝',
						age: '26'
					},
					{
						id: 2,
						name: '刘能',
						age: '20'
					},
					{
						id: 3,
						name: '小沈阳',
						age: '29'
					}
				]
			}
		},
		methods: {
			pointMe(num, e){
				console.log(num, e)
			}
		}
	}
</script>

<style>
</style>
