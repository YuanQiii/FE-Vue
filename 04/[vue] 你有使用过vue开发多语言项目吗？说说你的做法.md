# 你有使用过vue开发多语言项目吗？说说你的做法

- 安装 
> npm install vue-i18n

- 使用方法

1. 在 main.js 中引入 vue-i18n （前提是要先引入 vue）
```js
import VueI18n from 'vue-i18n'
Vue.use(VueI18n)
```

2. 准备本地的翻译信息
```js
const messages = {
    zh: {
      message: {
        hello: '好好学习，天天向上！'
      }
    },
    en: {
      message: {
        hello: 'good good study, day day up!'
      }
    }
}
```

3. 创建带有选项的 VueI18n 实例
```js
const i18n = new VueI18n({
    locale: 'en', // 语言标识
    messages
})
```

4. 把 i18n 挂载到 vue 根实例上
```js
const app = new Vue({
    router,
    i18n,
    ...App
}).$mount('#app')
```

5. 在 HTML 模板中使用
```html
<div id="app">
  <h1 style="font-size: 16px; text-align: center;">{{ $t("message.hello") }}</h1>
</div>
```