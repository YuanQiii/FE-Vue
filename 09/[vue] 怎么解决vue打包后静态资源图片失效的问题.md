# 怎么解决vue打包后静态资源图片失效的问题

1. 确定线上环境是否在根路径上，配置资源根目录，vue-cli2 和 vue-cli3 字段不一致（assetsPublicPath 和 publicPath ），如果项目是根路径上，用'/'，'./'都行，如果是在'/hc'这个路径上，用'./' 相对路径（需history模式），也可以用'/hc/'。 在'/hc'路径上，如果需要本地和线上保持一致，可以用环境做判断设置不同的publicPath值。
2. 确定静态文件放置的位置。
  ①. 如果放在public/static，不经过webpack打包， 放在public 又分使用绝对路径和相对路径。
  ②. 如果放在assets， 经过webpack打包， 使用的是相对路径
1. 路径是否是动态的，如果是动态，需要用require() 引入