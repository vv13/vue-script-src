<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <a href="https://webcert.cnmstl.net/cert/grade?sn=23e8abaade0745538be1a5971a6b9ddb" target="_blank" id="jvs-cert"></a>
    <vue-script-src src="https://cdn.bootcss.com/jquery/3.3.1/jquery.min.js"></vue-script-src>
    <vue-script-src src="https://webcert.cnmstl.net/cert/grade/small_h_img.js?sn=23e8abaade0745538be1a5971a6b9ddb"></vue-script-src>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import VueScriptSrc from '../dist/vueScriptSrc.umd'

export default {
  name: 'app',
  components: {
    HelloWorld,
    VueScriptSrc,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
