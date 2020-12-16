<template>
	<view>
		<view>样式</view>
		<view class="box1">这是一个样式<text class>文字文字</text></view>
		<view class="iconfont iconmeiyoushuju"></view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {

		}
	}
</script>

<style lang="scss">
	@import url("./a.css");
	
	.box1 {
		width: 375rpx;
		height: 375rpx;
		background: $uni-color-success;
		font-size: 30rpx;
		color: white;
		text{
			color: pink;
		}
	}
	
	
</style>
