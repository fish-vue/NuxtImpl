<template>
  <section>
    <!-- 返回响应的时候，模板已经被渲染完成了-->
    <div>{{text}}</div>

    <div>{{text2}}</div>
  </section>
</template>

<script>
export default {
  data(){
    return {
      text: 'some data from this.data.text'
    }
  },
  computed: {
    text2: function () {
      return 'some data from computed data'
    }
  }
}
</script>

