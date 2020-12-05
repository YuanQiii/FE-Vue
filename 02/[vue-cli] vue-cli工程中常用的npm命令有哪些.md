# vue-cli工程中常用的npm命令有哪些

1. - npm install：下载 node_modules 资源包的命令
2. - npm run dev：  启动 vue-cli 开发环境的 npm命令（3.0以下😔 ☞ 脚手架2启动方式）
   - npm run serve：启动 vue-cli 开发环境的 npm命令（3.0以上😀 ☛ 脚手架3启动方式）
3. - npm run build： vue-cli 生成 生产环境部署资源 的 npm命令（常说的打包文件）
   - 脚手架2打包，生成的是build文件
   - 脚手架3打包，生成的是dist文件
4. - serve build （脚手架2，把你写好的项目打包，然后在本机测试，查看是否完整）
   - serve dist  （脚手架3，把你写好的项目打包，然后在本机测试，查看是否完整）
5. - npm run build--report：用于查看 vue-cli 生产环境部署资源文件大小的 npm命令（脚手架2、3不一样）