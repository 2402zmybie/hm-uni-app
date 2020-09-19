16课: 全局共享数据: 
1 通过Vue的原型共享数据  Vue.prototype.baseURL = 'http://xxxx'
2 通过globalData共享数据: (微信小程序独有的)  getApp().globalData.text = 'test'
注: App.vue相当于小程序的 app.js

17课: 
插槽: 动态地给子组件传递标签

18课:
常用生命周期: 
	1 uni-app框架的生命周期结合了vue和微信小程序的生命周期
	2 全局App中使用onLaunch表示应用启动时
	3 页面中使用onLoad或者onShow分别表示 页面加载完毕时和页面显示时
	4 组件 中使用 mounted组件挂在完毕时, 其他的没有效果
	