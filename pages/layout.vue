<template>
  <section class="container">
    <Logo></Logo>
    <div>这个页面使用了自定义的layout</div>
  </section>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  // 引用自定义模板
  layout: 'custom'
}
</script>
