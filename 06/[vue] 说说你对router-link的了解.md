# 说说你对router-link的了解

- vue-router插件的其中一个组件, 用于跳转路由, 类似于a标签, 它一般也会渲染成a标签,
- 但是可以通过tag来变更默认渲染元素, 通过to来跳转

```html
// 字符串
<router-link to="apple"> to apple</router-link>
// 对象
<router-link :to="{path:'apple'}"> to apple</router-link>
// 命名路由
<router-link :to="{name: 'applename'}"> to apple</router-link>
// 直接路由带查询参数query，地址栏变成 /apple?color=red
<router-link :to="{path: 'apple', query: {color: 'red' }}"> to apple</router-link>
// 命名路由带查询参数query，地址栏变成/apple?color=red
<router-link :to="{name: 'applename', query: {color: 'red' }}"> to apple</router-link>
// 直接路由带路由参数params，params 不生效，如果提供了 path，params 会被忽略
<router-link :to="{path: 'apple', params: { color: 'red' }}"> to apple</router-link>
// 命名路由带路由参数params，地址栏是/apple/red
<router-link :to="{name: 'applename', params: { color: 'red' }}"> to apple</router-link>
```