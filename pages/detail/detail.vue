<template>
	<view>
		<!-- <view>
			<text>唱歌跳舞打篮球</text>
		</view>
		<view>
			<text selectable>唱歌跳舞打篮球</text>
		</view>
		<view>
			<text selectable space="ensp">唱歌    跳舞打篮球</text>
		</view>
		<view>
			<text selectable space="emsp">唱歌    跳舞打篮球</text>
		</view>
		<view>
			<text selectable space="nbsp" style="font-size: 30px;">唱歌    跳舞打篮球</text>
		</view>
		<view>
			<text selectable decode>&amp;</text>
		</view> -->
		<view>
			<view class="box" hover-class="box-active">唱歌跳舞打篮球</view>
		</view>
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

<style>
	.box{
		width: 10rem;
		background-color: #007AFF;
	}
	
	.box-active{
		background-color: red;
	}

</style>
