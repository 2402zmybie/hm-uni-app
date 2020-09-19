<template>
	<view class="content">
		<my-form>
			<!-- 动态传递标签 -->
			<input type="text" placeholder="插槽上显示的标签" />
			<radio></radio>
			<label>
				<checkbox :value="1" /><text></text>
			</label>
		</my-form>
	</view>
</template>

<script>
	import myForm from '@/components/my-form.vue'
	export default {
		components: {
			myForm
		},
		data() {
			return{
				
			}
		},
		methods:{
			
		},
		onLoad() {
			console.log("页面加载完毕");
		},
		onShow() {
			console.log("页面被看到")
		},
		
	}
</script>

<style lang="scss">

</style>
