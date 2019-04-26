<template>
  <div>
    <!--
    这是给所有的Pages用的，
    Pages的内容会被插入到<nuxt />里面。
    -->

    <!--这里我把Links放在这里，全局配置，方便调试-->
    <Links />

    <nuxt />
  </div>
</template>

<script>
import Links from '@/components/Links.vue'

export default {
  components: {
    Links
  }
}
</script>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}
</style>
