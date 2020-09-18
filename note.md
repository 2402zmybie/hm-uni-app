16课: 全局共享数据: 
1 通过Vue的原型共享数据  Vue.prototype.baseURL = 'http://xxxx'
2 通过globalData共享数据: (微信小程序独有的)  getApp().globalData.text = 'test'
注: App.vue相当于小程序的 app.js

17课: 
插槽: 动态地给子组件传递标签