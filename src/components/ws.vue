<template>
  <div class="ws">
    <div>{{title}}</div>
    <div>{{subtitle}}</div>
    <div @click="handleChange">change</div>
    <div id="app1">
        <span v-bind:title="message">鼠标悬停几秒钟查看此处动态绑定的提示信息！</span>
    </div>
    <div id="app2">
        <p v-if="seen">现在你看到我了</p>
        <p v-else>Oh no</p>
    </div>
    <div id="app3">
            <wsplus v-for="i in todos" :key='i'>
            </wsplus>
    </div>
    <div id="app4">
        <p>{{message1}}</p>
        <button @click="reverseMessage">反转消息</button>
    </div>
    <div id="app5">
        <p>{{message2}}</p>
        <input v-model="message2">
    </div>
    <div id="app6">
        <p v-show="ok">wow</p>
        <p v-if="loginType === 'username'">
        <label>Username</label>
        <input placeholder="Enter your username" key="username-input">
        </p>
        <p v-else>
        <label>Email</label>
        <input placeholder="Enter your email address" key="email-input">
        </p>
        <button @click="switchover">切换</button>
    </div>
  </div>
</template>

<script>
import wsplus from './wsplus.vue'
export default {
  name: 'WS',
  components: {
    wsplus,
  },
  data() {
    return {
      title: '第一部分',
      subtitle: '副标题',
      message: '页面加载于' + new Date().toLocaleString(),
      seen: false,
      todos:[
          {text:'js'},
          {text:'js1'}
      ],
      message1: 'Hello Vue.js!',
      message2: 'banana',
      loginType: 'username',
      ok:true
    }
  },
  mounted() {
    this.title = '加载完毕！！'
  },
  methods: {
    handleChange() {
      this.subtitle = '副标题已经改变！'
    },
    reverseMessage() {
      this.message1 = this.message1.split('').reverse().join('')
    },
    switchover() {
      if(this.loginType =='username'){
        this.loginType='password'
      }else{
        this.loginType='username'
      }
    }
  }
}
</script>

<style scoped>
.ws {
  background: #34343455;
  color: #000000;
}
</style>
