# NuxtImpl

## 实践


## 目录介绍
nuxt会根据文件目录来配置我们的项目，这一点非常重要。
创建相关目录就会自动开启配置。
#### pages
这个目录下就放置我们的vue文件，每个文件都会被打包成一个页面。
Nuxt.js 会依据 pages 目录中的所有 *.vue 文件生成应用的路由配置。

- GET /  
  返回index.vue页面
- GET /login
  返回login.vue页面
  
#### components
放置项目的一些组件，在pages中可以通过类似于
```js
import Logo from '~/components/Logo.vue'
```
之类的命令来引用。

#### layout
包裹了pages，一般把全局公共组件放到这里

#### assert
和Vue中一样，放置组件依赖的资源文件

#### 目录别名
为了方便文件之间的互相引用，nuxt编译时提供了几个简写
- `~` 或 `@`: src目录
- `~~` 或 `@@`: 根目录

## Build Setup

``` bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout [Nuxt.js docs](https://nuxtjs.org).

## 环境搭建
```bash
# 安装脚手架
$ npm i create-nuxt-app

# 初始化项目
$ npx create-nuxt-app NuxtImpl

# 启动开发环境
$ cd NuxtImpl
$ npm run dev
```
启动后，nuxt便开始监听3000端口。
Nuxt.js 会监听 pages 目录中的文件更改，
因此在添加新页面时无需重新启动应用程序。
