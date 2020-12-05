# vue-router怎么配置404页面

```js
export default {
    path: '*',
    name: '404',
    component: '组件404',
}
```

> 需注意：将改路由配置放到所有路由的配置信息的最后，否则会其他路由path匹配造成影响