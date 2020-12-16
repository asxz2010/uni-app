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
		<view class="box2" hover-class="box2-active">
			<view class="box" hover-class="box-active" hover-stay-time="2000" hover-start-time="2000" hover-stop-propagation>唱歌跳舞打篮球</view>
		</view>
		<button>按钮</button>
		<button size="mini">按钮</button>
		<button type="primary">按钮</button>
		<button type="primary" plain>按钮</button>
		<button type="primary" plain disabled>按钮</button>
		<button loading></button>
		<image src="https://scpic2.chinaz.net/Files/pic/pic9/202012/apic29399_s.jpg"></image>
		<image src="https://scpic2.chinaz.net/Files/pic/pic9/202012/apic29399_s.jpg" mode="aspectFit" class="img1"></image>
		<image src="https://scpic2.chinaz.net/Files/pic/pic9/202012/apic29399_s.jpg" mode="aspectFill"></image>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {

		},
		onLoad(options){
			console.log(options)
		}
	}
</script>

<style>
	.img1{
		width: 20rem;
		height: 20rem;
	}
	
	.box{
		width: 10rem;
		background-color: #007AFF;
	}
	
	.box-active{
		background-color: red;
	}
	
	.box2{
		width: 200px;
		height: 200px;
		background: blue;
	}
	
	.box2-active{
		background: pink;
	}

</style>
