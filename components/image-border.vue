<template>
	<view>
		<image :src="src" mode="widthFix" @tap="handleImageClick(src)"></image>
	</view>
	
</template>

<script>
	export default {
		props:{
			src:String
		},
		methods:{
			handleImageClick(src) {
				this.$emit("handleImageClick",src)
			}
		},
	}
</script>

<style>
</style>
