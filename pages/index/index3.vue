<template>
	<view class="content">
		<view>{{ title }}</view>
		<view>{{ money }}</view>
		<view>{{ isRich }}</view>
		<view>{{ person.name }}</view>
		<view>{{ person.skill }}</view>
		
		<!-- 在标签上通过属性的方式来使用数据 -->
		<view :data-color="color">color</view>
		<view>---------循环-----------</view>
		<!-- 循环 -->
		<view v-for="(item,index) in list" :key="index">{{ item.id }}======={{ item.name }}</view>
		<view>----------显示隐藏----------</view>
		<!-- 显示隐藏  v-if适用于不频繁切换显示隐藏,  v-show适用于频繁切换-->
		<template v-if="vIfShow">
			<view>vIfShow</view>
		</template>
		<template v-show="vShowShow">
			<view>vShowShow</view>
		</template>
		<view>----------计算属性----------</view>
		<view>{{ usMoney }}</view>
		<view>----------计算属性之过滤数组----------</view>
		<block v-for="(item,index) in filterList" :index="index">
			<view>{{ item.name }}</view>
		</block>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello',
				money:100,
				isRich:false,
				person: {
					name:"孙悟空",
					skill:"72变"
				},
				color: "aqua",
				list: [
					{id:1, name:"苹果"},
					{id:2, name:"樱桃"},
					{id:3, name:"香蕉"}
				],
				vIfShow:false,
				vShowShow:true
			}
		},
		computed:{
			//把 usMoney看成是在data中的普通的数据一样来使用即可
			usMoney() {
				return "$" + this.money
			},
			//过滤数组
			filterList() {
				//数组中id>1的都不显示
				return this.list.filter(it=> it.id <= 1)
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">

</style>
