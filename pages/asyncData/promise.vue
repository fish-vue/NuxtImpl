<template>
  <section>
    <div>{{JSON.stringify(data)}}</div>
  </section>
</template>

<script>
import axios from 'axios'

let url = 'https://api.github.com/orgs/fish56'

export default {
  data(){
    return {
    }
  },

  // 通过Promise异步调用
  //   等到接受数据后才会开始渲染，并返回页面
  asyncData(){
    return axios.get(url)
      .then(res => {
        return {
          data: res.data
        }
      })
  }
}
</script>

