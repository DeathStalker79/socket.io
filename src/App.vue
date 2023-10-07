<template>
  <div id="app">
<!--  <div>{{socket}}</div>-->
  </div>
</template>

<script>
const {io} = require("socket.io-client");
// eslint-disable-next-line no-unused-vars
const socket = io("http://localhost:3001");

export default {
  name: 'App',
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
