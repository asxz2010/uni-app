<template>
	<view class="content">
		<!-- <image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">{{ title }}</text>
		</view> -->

		<test v-if="flag" :title="title" @getNum="getNum"></test>
		<button type="primary" @click="checkTest">切换</button>
		<view>这是子组件传过来的值:{{ num }}</view>
		<testA></testA>
		<testB></testB>
		<uniCalendar :insert="true" :lunar="true" :start-date="'2019-3-2'" :end-date="'2021-5-20'" @change="change"></uniCalendar>
	</view>
</template>

<script>
	import test from '../../components/test.vue'
	import testA from '../../components/testA.vue'
	import testB from '../../components/testB.vue'
	import uniCalendar from '@/components/uni-calendar/uni-calendar.vue'

	export default {
		data() {
			return {
				title: 'Hello',
				flag: true,
				num: 0,
			}
		},
		methods: {
			checkTest() {
				this.flag = !this.flag
			},
			getNum(num) {
				console.log('num:' + num)
				this.num = num
			},
			change(e){
				console.log(e)
			}
		},
		onLoad(options) {
			console.log('页面加载了' + options)
		},
		onShow() {
			console.log('页面显示了')
		},
		onReady() {
			console.log('页面初次渲染完成')
		},
		onHide() {
			console.log('页面隐藏了')
		},
		components: {
			test,
			testA,
			testB,
			uniCalendar
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
