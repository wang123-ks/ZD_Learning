<template>
  <div id="app">{{message}}</div>
</template>

<script>
export default {
  name: 'plus',
  data() {
    return {
      message: 'Hello Vue!'
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