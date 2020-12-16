# 怎么解决vue动态设置img的src不生效的问题

- 因为动态添加src被当做静态资源处理了，没有进行编译，跟打包工具有关，所以要加上require
- > \<img :src="require('@/assets/images/xxx.png')" />
- 直接用 script 的形式引入vue没有问题