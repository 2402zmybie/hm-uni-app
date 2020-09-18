<template>
	<view class="content">
		<view data-index="11" @tap="clickEvent(1,$event)">点击我试试1</view>
		<view data-index="22" @tap="clickEvent(2,$event)">点击我试试2</view>
	</view>
</template>

<script>
	export default {
		data() {
			return{
				
			}
		},
		methods:{
			//$event是固定写法
			clickEvent(index,e) {
				console.log(index)
				console.log(e)
				//取出自定义属性的值
				console.log(e.currentTarget.dataset.index)
			}
		},
		onLoad() {

		}
	}
</script>

<style lang="scss">

</style>
