<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <LikeNumber :total-number="number" @my-click="incrementNumber" @my-click2="incrementNumber2"></LikeNumber>
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
    incrementNumber(num, value1, value2, value3) {
      console.log(value1);
      console.log(value2);
      console.log(value3);
      this.number = num;
    },
    incrementNumber2(value) {
      console.log(value);
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
