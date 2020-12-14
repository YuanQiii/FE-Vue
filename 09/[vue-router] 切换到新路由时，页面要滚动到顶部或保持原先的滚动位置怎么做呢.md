# 切换到新路由时，页面要滚动到顶部或保持原先的滚动位置怎么做呢

- 滚动到顶部：在new Router()的时候，配置
```js
scrollBehavior(ro,form,savedPosition){
//滚动到顶部
return {x:0,y:0}
//保持原先的滚动位置
return {selector：falsy}
}
```