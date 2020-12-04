# 从0到1自己构架一个vue项目，说说有哪些步骤、哪些重要插件、目录结构你会怎么组织

## 普通vue.js项目
- 引入\<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js">\</script>
- 在代码架构上变为数据和模型分离的模式即可

## vue-cli

- 创建项目默认
- 一般会额外创建views，components，api，utils，stores等
- 下载重要插件，比如axios，dayjs（moment太大），其他的会根据项目需求补充
- 封装axios，统一api调用风格和基本配置
- 如果有国际化需求，配置国际化
- 开发，测试和正式环境配置，一般不同环境API接口基础路径会不一样

[详细回答](https://github.com/haizlin/fe-interview/issues/983#issuecomment-546895784)