<template>
  <section>
    <div>{{data}}</div>
  </section>
</template>

<script>
export default {
  data(){
    return {
    }
  },

  // 返回值是普通object，直接融入data对象中
  //   因为是在组件初始化前拿到数据，所以函数里面拿不到当前vue实例
  asyncData(){
    return {
      data: 'fetch a object'
    }
  }
}
</script>

