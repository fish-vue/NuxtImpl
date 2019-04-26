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

  // 使用async/await
  async asyncData(){
    let { data } = await axios.get(url)
    return {
      data: data
    }
  }
}
</script>

