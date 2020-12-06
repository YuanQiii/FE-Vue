# 在使用vue-cli开发vue项目时，自动刷新页面的原理你了解吗

自动刷新页面并不是vue-cli的功能，而是webpack的hot-module-replacement-plugin插件在做这件事，这个插件是webpack自带的插件，用来做hmr的。如果需要配置hmr只需要在webpack.config.js的devServer字段写 下面的配置即可
```js
{
contentBase: 服务器可以访问的根目录,
hot:true, //开启热模块替换也就是hmr
hotOnly:true //不刷新页面，只做hmr
}
```

而由于vue-cli3集成了webpack的配置，所以vue.config.js里面也有这个属性，配置写法是一样的