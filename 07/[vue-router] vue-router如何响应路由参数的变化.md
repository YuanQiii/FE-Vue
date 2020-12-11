# vue-router如何响应路由参数的变化

- 切换路由，路由参数发生了变化，但是页面数据并未及时更新，需要强制刷新后才会变化
- 不同路由渲染相同的组件时（组件复用比销毁重新创建效率要高），在切换路由后，当前组件下的生命周期函数不会再被调用

1. 使用 watch 监听
```js
watch: {
    $route(to, from){
        if(to != from) {
            console.log("监听到路由变化，做出相应的处理");
        }
    }
}
```

2. 向 router-view 组件中添加 key
```html
<router-view :key="$route.fullPath"></router-view>
```
 - $route.fullPath 是完成后解析的URL，包含其查询参数信息和hash完整路径
 - 防止组件复用