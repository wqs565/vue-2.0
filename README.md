# vue_project

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```
# 自己搭建环境：

Homebrew 1.0.6(Mac)、Node.js 6.7.0、npm 3.10.3、webpack 1.13.2、vue-cli 2.4.0、Atom 1.10.2

# 安装环境
```
# 打开终端运行以下命令

# 安装brew（Windows 跳过这步）

/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
# 安装 nodejs

Windows 下直接下载安装包即可。Mac 的安装步骤如下：

(node:42) fs: re-evaluating native module sources is not supported.
用 npm install npm@3.10.3 更新 npm 版本报错:

(node:42) fs: re-evaluating native module sources is not supported.
解决办法:在官网下载6.70的安装包再安装一次(刚刚相当于帮你配置好环境变量，现在再安装一次升级到最新的 npm)

好像以前官网的安装包不会自动配置环境变量的，由于我电脑上之前安装过 nodejs 所以环境变量已经配置好了，不知道现在的安装包会不会自动配置环境变量。

# 获取nodejs模块安装目录访问权限（Windows 跳过此步）

sudo chmod -R 777 /usr/local/lib/node_modules/
# 安装淘宝镜像

npm install -g cnpm --registry=https://registry.npm.taobao.org
# 安装webpack

cnpm install webpack -g
# 安装vue脚手架

npm install vue-cli -g
在硬盘上找一个文件夹放工程用的，在终端中进入该目录

# Mac

cd 目录路径
根据模板创建项目

vue init webpack-simple 工程名字<工程名字不能用中文>或者创建 vue1.0 的项目vue init webpack-simple#1.0 工程名字<工程名字不能用中文></工程名字不能用中文></工程名字不能用中文>
会有一些初始化的设置，如下输入:Target directory exists. Continue? (Y/n)直接回车默认(然后会下载 vue2.0模板，这里可能需要连代理)Project name (vue-test)直接回车默认Project description (A Vue.js project) 直接回车默认Author 写你自己的名字

cd 命令进入创建的工程目录

工程目录如图所示:查看图片

# 安装项目依赖
一定要从官方仓库安装，npm 服务器在国外所以这一步安装速度会很慢。

npm install
不要从国内镜像cnpm安装(会导致后面缺了很多依赖库)

cnpm install
# 安装 vue 路由模块vue-router和网络请求模块vue-resource

cnpm install vue-router vue-resource --save
# 启动项目

npm run dev
填坑(以下坑可能由于 vue2.0 导致其他相关编译打包工具没更新导致的)

<strong>【重点】后来发现这些坑是由于 npm 不是最新的版本3.10.2， 用 npm 3.9.5就会出现以下坑</strong>解决办法: 请运行以下命令<strong>npm update -g</strong>
报错

Error: Cannot find module 'opn'Error: Cannot find module 'webpack-dev-middleware'Error: Cannot find module 'express'Error: Cannot find module 'compression'Error: Cannot find module 'sockjs'Error: Cannot find module 'spdy'Error: Cannot find module 'http-proxy-middleware'Error: Cannot find module 'serve-index'
# 如果你用的是老版本的 vue-cli 还可能报其他错误，需要更新一下 vue-cli

npm update vue-cli
然后可以查看一下当前全局 vue-cli 的版本

npm view vue-cli
安装一下这个依赖到工程开发环境

cnpm install opn --save-devcnpm install webpack-dev-middleware --save-devcnpm install express --save-devcnpm install compression --save-devcnpm install sockjs --save-devcnpm install spdy --save-devcnpm install http-proxy-middleware --save-devcnpm install serve-index --save-devcnpm install connect-history-api-fallback --save-dev
再启动项目，报错

ERROR in ./src/main.jsModule build failed: Error: Cannot fi...
安装一下 babel-runtime

cnpm install babel-helpers --save-dev
启动项目，再次报错

Module build failed: Error: Cannot find ...
找不到依赖那就再安装一下

cnpm install babel-helpers --save-devcnpm install babel-traverse --save-devcnpm install json5 --save-dev.<strong>..不写了，请把全部把旧的环境全部清除，更新到最新版本</strong>
解决办法概述

# 遇到

# Module build failed: Error: Cannot find module '模块名'
# 那就安装

cnpm install 模块名 --save-dev(关于环境的，表现为npm run dev 启动不了)cnpm install 模块名 --save(关于项目的，比如main.js，表现为npm run dev 成功之后控制台报错)比如escape-string-regexp、strip-ansi、has-ansi、is-finite、emojis-list
终于可以启动项目了

输入完命令会自动启动浏览器，如果默认打开 IE 不行

# npm run dev
```

For detailed explanation on how things work, consult the [docs for vue-loader](http://vuejs.github.io/vue-loader).
