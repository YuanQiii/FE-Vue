# vue-router有哪几种导航钩子（ 导航守卫 ）

- 三种
1. 全局守卫：beforeEach,afterEach
2. 路由独享守卫：beforeEnter
3. 组件级别的守卫:beforeRouteEnter,beforeRouteUpdate,beforeRouteLeave

- 他们执行顺序：全局 -> 路由 ->组件

- 除了afterEach全局后置外，其他的守卫中务必要调用next(),否则无法完成导航
- 还有注意全局前置守卫可以用来进行拦截，（登录拦截）