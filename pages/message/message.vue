<template>
	<view>
		<button type="primary" @click="chooseImage">上传图片</button>
		<image v-for="img in imgArr" :src="img" @click="previewImage(current)"></image>
		
		<!-- #ifdef H5 -->
		<view>只在h5中显示</view>
		<!-- #endif -->
		
		<!-- #ifdef MP-WEIXIN -->
		<view>只在微信小程序中显示</view>
		<!-- #endif -->
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				imgArr: []
			}
		},
		methods: {
			chooseImage(){
				uni.chooseImage({
					count: 5,
					success: res=>{
						this.imgArr = res.tempFilePaths
						console.log(res)
					}
				})
			},
			previewImage(current){
				uni.previewImage({
					current,
					urls: this.imgArr,
				})
			}
		},
		onLoad() {
			// #ifdef H5
			console.log('只在H5中输出打印')
			// #endif
			// #ifdef MP-WEIXIN
			console.log('只在微信小程序中输出打印')
			// #endif
		}
	}
</script>

<style>
	
	/* #ifdef H5*/
	view{
		color: hotpink;
	}
	/* #endif */
	/* #ifdef MP-WEIXIN  */
	view{
		color: blue;
	}
	/* #endif */

</style>
