<template>
  <div id="app">
    <WS></WS>
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <WSPLUS></WSPLUS>
  </div>
</template>

<script>

import HelloWorld from './components/HelloWorld.vue'
import WS from './components/ws.vue'
//import WSPLUS from './components/wsplus.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    WS,
 //   WSPLUS
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
