# vue-cli怎么解决跨域的问题

- vue-cli无法解决跨域问题。真正解决跨域问的是webpack
- 只不过vue-cli3.0将webpack的配置继承到了vue.config.js中
- 在根目录下新建：vue.config.js注意名不能错误，然后里面配置
```js
module.exports = {
  devServer: {
    proxy: {
      //配置跨域
      '/api': {
        target: '跨域url',
        ws: true,
        changOrigin: true
        // pathRewrite: {
        // '^/api': ''
        // }
      }
    }
  }
}
```