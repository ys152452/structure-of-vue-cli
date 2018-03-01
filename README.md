# vue-demo

>vue项目的vue-cli初步搭建，均为默认配置命名
## 1.环境配置
### 相关环境版本号
- node v9.3.0
- npm v5.5.1
- webpack v2.2.1
### 开发软件
- VSCode
## 2.项目搭建
> 此处可参考[vue官方文档](https://cn.vuejs.org/v2/guide/installation.html)
``` bash
# 全局安装 vue-cli
$ npm install --global vue-cli
# 创建一个基于 webpack 模板的新项目
$ vue init webpack vue-demo
$ cd vue-demo
# 安装依赖
$ npm install
```
## 3.npm常用命令
``` bash
# 安装依赖
npm install
# 运行项目
npm run dev
# 打包
npm run build
# 安装依赖到项目本地
npm install abc --save-dev
```
## 4.项目目录结构
> vue-demo<br>
<br>+build &nbsp;&nbsp;&nbsp;&nbsp;<i>构建相关配置</i><br>
<br>+config &nbsp;&nbsp;&nbsp;&nbsp;<i>开发环境配置</i><br>
<br>+dist &nbsp;&nbsp;&nbsp;&nbsp;<i>打包后生成的目录</i><br>
<br>+node_modules &nbsp;&nbsp;&nbsp;&nbsp;<i>本地依赖包安装目录</i><br>
<br>-src &nbsp;&nbsp;&nbsp;&nbsp;<i>开发目录</i><br>
<br>--assets &nbsp;&nbsp;&nbsp;&nbsp;<i>静态资源目录(src中需要使用到的静态资源，各类图标图片、CSS文件等)</i><br>
<br>--components &nbsp;&nbsp;&nbsp;&nbsp;<i>组件开发目录</i><br>
<br>--router &nbsp;&nbsp;&nbsp;&nbsp;<i>路由文件配置，可参考[vue-router文档](https://router.vuejs.org/zh-cn/essentials/getting-started.html)</i><br>
<br>--App.vue &nbsp;&nbsp;&nbsp;&nbsp;<i>加载到index.html中的入口组件，可做登录页或者公用页</i><br>
<br>--main.js &nbsp;&nbsp;&nbsp;&nbsp;<i>js入口文件，功能引入和new Vue实例,以及一些简单初始化js配置</i><br>
<br>+static &nbsp;&nbsp;&nbsp;&nbsp;<i>静态资源目录(字体文件，标签引入的文件等)</i><br>
<br>package.json &nbsp;&nbsp;&nbsp;&nbsp;<i>安装在本地的全部依赖包信息</i><br>
<br>...
## 5.注意事项
* npm install时可选用cnpm
* build中(webpack.base.conf.js)配置webpack，常用：jquery引入时alias中定义$符，loader配置等
* config中(index.js)配置运行，常用：端口号，assetsPublicPath的配置（build之后assets和static中静态资源404问题）
* package.json中可能未包含npm全局安装的依赖
* 功能单一的插件使用标签引入cdn比import更利于打包后的体积优化
* src中的结构可以根据实际自行变动