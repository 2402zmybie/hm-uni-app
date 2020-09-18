<template>
	<view class="content">
		<view >图片地址: {{ srcImageUrl }}</view>
		<image-border :src="src1" @handleImageClick="handleImageClick"></image-border>
		<image-border :src="src2" @handleImageClick="handleImageClick"></image-border>
	</view>
</template>

<script>
	import imageBorder from '@/components/image-border.vue'
	export default {
		components: {
			imageBorder
		},
		data() {
			return{
				srcImageUrl: "",
				src1:"https://dss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=2093143442,3189902132&fm=26&gp=0.jpg",
				src2:"https://dss1.bdstatic.com/70cFvXSh_Q1YnxGkpoWK1HF6hhy/it/u=3380212121,1825347810&fm=111&gp=0.jpg"
			}
		},
		methods:{
			handleImageClick(src) {
				this.srcImageUrl = src
			}
		},
		onLoad() {
			//得到全局的数据
			console.log("vue原型定义的全局数据: " + this.baseUrl)
			
			console.log("获取小程序独有的全局数据(但是在app中也能得到) globalData:" + getApp().globalData.base)
		}
	}
</script>

<style lang="scss">

</style>
