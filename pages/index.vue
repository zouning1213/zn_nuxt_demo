<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title"> 
        <nuxt-link to="/home-list">home-list-------to</nuxt-link>
        <nuxt-link to="/goods_list/goods_list">list</nuxt-link>
      </h1>
      <h2 class="subtitle">
        My glorious Nuxt.js project1
      </h2> 
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  asyncData(context){
    // context.app.myInjectedFunction('ctx!')
    // try {
    //   throw new Error()
    // } catch {
    //   // context.$errorHandler({statusCode: 500, message: '服务器开小差了~' })
    // }
  },
  mounted(){
    
      this.showLoginError()
  },
  notifications: {
    showLoginError: { // You can have any name you want instead of 'showLoginError'
      title: '提示标题',
      message: 'message内容 Failed to authenticate',
      type: 'success' // You also can use 'VueNotifications.types.error' instead of 'error'
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
