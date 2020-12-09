# vue-cli生成的项目可以使用es6、es7的语法吗？为什么

- 有些可以直接使用, 有些不行
- 根据vue-cli 3.0的配置, 如果webpack能检测到, 它会自动把垫片自动打包到vendor中, 但是有些特性它检测不出来, 如es6.promise