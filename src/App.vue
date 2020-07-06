<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <LikeNumber :total-number="number" @my-click="incrementNumber"></LikeNumber>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import LikeNumber from './components/LikeNumber.vue'

export default {
  name: 'App',
  data() {
    return {
      number: 14
    };
  },
  components: {
    HelloWorld,
    LikeNumber
  },
  methods: {
    incrementNumber(value) {
      this.number = value;
    }
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
