<template>
	<view class="content">
		<my-form>
			<!-- 动态传递标签 -->
			<input type="text" placeholder="插槽上显示的标签" />
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
			
		}
	}
</script>

<style lang="scss">

</style>
