<template>
  <div class="links-container">
    <!-- 类似于router-link, 直接加载需要的其他组件 -->
    <nuxt-link to="/">/</nuxt-link>
    <nuxt-link to="/login">/login</nuxt-link>
    <nuxt-link to="/data">/data</nuxt-link>
    <nuxt-link to="/layout">/layout</nuxt-link>
    <nuxt-link to="/asyncData/object">/asyncData/object</nuxt-link>
    <nuxt-link to="/asyncData/promise">/asyncData/promise</nuxt-link>
    <nuxt-link to="/asyncData/await">/asyncData/await</nuxt-link>

    <!-- 页面跳转，或导致页面重新渲染 -->
    <a href="/login">a-link to /login</a>
  </div>
</template>

<style scoped>
  .links-container {
    margin: 0 auto;
    display: flex;
    align-items: center;
    text-align: center;
    flex-direction: column;
    max-height: 300px;
  }
</style>
