# To do list

## vue

### 使用疑问

1. 以下两种写法有什么不同？

```
new Vue({
 el: '#app',
 router,
 template: '<App/>',
 components: { App },
 store: vuex,
})
// 新写法
new Vue({
 router,
 store: vuex,
 render: h => h(App),
}).$mount('#app')
```

2. 新版 vue 3.0 创建根实例 creatApp 多个实例如何相互通信

- 比如摇一摇模块 共用了 wall 模块的内容 一个模块一个 app，该如何处理？

3. 函数式组件 使用条件？

   无状态、无实例 functional: true 渲染开销低
   在 3.x 中，函数式组件 2.x 的性能提升可以忽略不计，这个可忽略

4. 重新理解生命周期

### 深入

1. 核心：Vue.js 框架中的 Virtual DOM 剖析

   什么是 Virtual DOM 和 Snabbdom？

   如何深度掌握 Virtual DOM 源码结构以及核心函数实现？

   patch 函数以及 Diff 算法的整个实现过程是怎样的？

   彻底搞定 Virtual DOM 中的模块机制。

2. 实战：手写一个属于自己的 Vue.js 数据响应式框架

   响应式数据的优势是什么？是如何实现的？

   如何使用 Observer 将数据转换成响应式数据？

   如何使用 Dep 收集依赖、发送通知？

   如何掌握用 Watcher 监听数据，自动更新视图？

3. 进阶：Vue.js 框架如何实践服务端渲染方案？

   掌握服务端渲染（SSR）核心解决的问题

   掌握使用 Nuxt.js 框架开发的最佳实践

   掌握 Nuxt.js 框架使用中的 SEO 优化处理

   掌握同构开发模式以及同构应用中的状态激活

   了解同构类型应用的发布与自动化部署

4. 优化：Vue 的长列表虚拟滚动
5. Vue 热点面试题

### vue3

- 组合式 API：setup 传入 props return 参数 ref() toRefs()
- teleport

### 单元测试

### mockjs 使用

### 统一错误处理

## typescript

## Hi 现场 3.0

### 每个模块建立一个根实例 creatApp

1. 每个模块独立的 vuex 需要一个全局的模块存放全局的 vuex

### 模块和组件的关系

## 前端自动化

### webpack 到底都干了什么？

1. babel 编译 es5 -> es6
2. 运行环境
3. 压缩图片和压缩代码
4. 按需打包

## Node.js 全栈

## ES6 & Javascript 的深入理解

### 闭包

### 深拷贝和浅拷贝的问题

## React

### React one

1. 起源于 Facebook 学习得是 4.x 版本 设计思想独特 javascript MVC

   - library（库）：小而巧，只提供特定得 api；船小好掉头，可以方便得从一个库切换到另外得库；但是代码几乎不会改变
   - Framework（框架）：大而全；提供了一整套得解决方案；所以在框架中间切换比较困难

2. 前端三大主流框架：Angular.js 最早 Vue.js 最火 React 最流行
3. React 与 Vue 的对比

   - 组件化

     1. 什么是模块化：是从**代码**角度的分析的；把一些可复用的代码抽离未单个模块；便于项目的维护和开发
     2. 什么是组件化：是从**UI 界面**的分析的；把一些可复用的 UI 元素抽离未单个组件；便于项目的维护和开发
     3. 组件化的好处：随着项目规模的增大，手里的组件越来越多；很方便就能把现有的组件拼接为一个完整的页面；
     4. Vue 如何实现组件化：通过.vue 文件创建对应组件
     5. React 如何实现组件化：React 中有组件化概念，但是没有 vue 这样组件模板文件；React 中，一切都是以 js 来表现的；因此，ES6 和 ES7（async 和 await）要会用

   - 开发团队

4. React 中几个核心概念
   - 虚拟 DOM（Virtual Document Object Model）
     - DOM：浏览器中的概念
     - 虚拟 DOM 是框架中的概念
     - 虚拟 DOM 是为了实现页面元素的高速更新,本质是用 js 对象模拟 DOM 元素和嵌套关系
   - Diff 算法
     - tree diff:Dom 树的逐层对比
     - component diff:
     - element diff:

## 微前端框架 qiankun

<https://qiankun.umijs.org/zh>

## 主题设计方案

### 如何设计主题配置
