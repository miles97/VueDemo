## babyshark养成

### 目前技术栈以及个人能力分析

目前掌握的基本技能就是vue 原生小程序开发  uni-app  以及部分原生h5加jquery gulp 等简单技能

vue和小程序擅长的是echarts绘制，并偏向移动端。项目工程化的内容了解的领域比较见谅。

uni-app开发过一个项目，h5原生以及jq涉及的东西实际上也不深刻。

接下来的学习路径其实是搞清楚主要是vue中的若干组件的核心功能和正确使用，然后对于一些正确的使用功能进行偏正
此外进行主流框架的了解，其实就是react以及简单的flutter起手，学习的目的简单的来说就是可以让学习曲线可能的攀升一点，同时也可以了解未来原声项前端的构建工程化。

距离国庆还有一个月，目前的学习计划就是看看开源的react代码然后跟着写一点简单的页面demo，然后整体的了解使用react基本的应用相关的组件，redux以及组件间通信等核心的应用层面关系，每天了解两个小时后基本一个月后9月中简单的重定向。


## uniapp开发小结

* 使用前端的split进行模糊匹配搜索

使用@input="confirm" 首先监听输入内容
```js
let value = e.detail.value
this.keyword = value
this.haveValue = true
let self = this;
	if(value){
		let attr = [];
		let obj= {};
		for(let item in self.thatOptions){
			if(self.thatOptions[item].city.indexOf(value)> -1){
				obj = {
					city: self.thatOptions[item].city,
					id: self.thatOptions[item].id,
					code: self.thatOptions[item].code
				}
				attr.push(obj)
			}
			
		}
		self.searchList = attr;
	}else{
		self.searchList = self.thatOptions
	}
	var search = this.search;
```

* 兼容性问题排查

使用window.alert()，通过本地代理localhost跑的本地ip以及端口在其他移动设备上调试。//简单的逻辑

## typescript使用小结分享



## 生产力相关优化

编辑器效率低下，考虑使用vscode集成相关应用

使用mac编程后注意事项以及行为养成习惯

## 简单的react起步学习 

通过网课等学习进行整体的框架搭建意识，了解更多的生态以及代码规范

目前阶段的react实战以及学习，大概掌握了简单的react页面构建的基本方法，但是对于组件化的思维方式还是有局限性，特别是掌握能力以及实践方面还是没能大力构建。

基本的生命周期也是一知半解，目前两天时间里面需要精进的东西还是更多对于react高级组件的使用以及基本用法的快速熟悉，目前来说，react使用上面和vue项目的差别还是有限。

今天和明天直接啃简单的应用上面，对于什么路由以及最基础的传值，组件生命周期以及页面等等直接实践，最后直接看文档总结跟vue之间的差别来着，直接整简单的技术栈实践来着。