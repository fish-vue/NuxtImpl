# Pages

其实，之前对比PHP和node的时候我就在想，node比PHP更加适合作为脚本语言和前端
代码混合开发。
这里我们的Page就是最终的页面，类似于PHP模板。

页面之间的跳转是需要重新加载页面的

## 基础路由
假设 pages 的目录结构如下：

```
pages/
--| user/
-----| index.vue
-----| one.vue
--| index.vue
```
那么，Nuxt.js 自动生成的路由配置如下：

```js
router: {
  routes: [
    {
      name: 'index',
      path: '/',
      component: 'pages/index.vue'
    },
    {
      name: 'user',
      path: '/user',
      component: 'pages/user/index.vue'
    },
    {
      name: 'user-one',
      path: '/user/one',
      component: 'pages/user/one.vue'
    }
  ]
}
```

## 动态路由
在 Nuxt.js 里面定义带参数的动态路由，
需要创建对应的以下划线作为前缀的 Vue 文件 或 目录。

以下目录结构：

pages/
--| _slug/
-----| comments.vue
-----| index.vue
--| users/
-----| _id.vue
--| index.vue
Nuxt.js 生成对应的路由配置表为：

router: {
  routes: [
    {
      name: 'index',
      path: '/',
      component: 'pages/index.vue'
    },
    {
      name: 'users-id',
      path: '/users/:id?',
      component: 'pages/users/_id.vue'
    },
    {
      name: 'slug',
      path: '/:slug',
      component: 'pages/_slug/index.vue'
    },
    {
      name: 'slug-comments',
      path: '/:slug/comments',
      component: 'pages/_slug/comments.vue'
    }
  ]
}
你会发现名称为 users-id 的路由路径带有 :id? 参数，表示该路由是可选的。如果你想将它设置为必选的路由，需要在 users/_id 目录内创建一个 index.vue 文件。

：API Configuration generate

警告：generate 命令会忽略动态路由: API Configuration generate
