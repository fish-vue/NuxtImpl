<template>
  <section class="container">
    <div>
      Hello, 这里是动态路由界面:
            /routes/var/slugs/:slug/
    </div>

    <button @click="slug">获得当前页面的slug参数</button>
  </section>
</template>

<script>
export default {
  methods:{
    slug: function (){
      alert(this.$route.params['slug'])
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
