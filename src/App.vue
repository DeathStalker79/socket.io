<template>
  <div id="app">
    <nav>
      <router-link to="/home">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/">Test</router-link>
    </nav>
    <router-view></router-view>
  </div>
</template>

<script>
const {io} = require("socket.io-client");
// eslint-disable-next-line no-unused-vars
const socket = io("http://localhost:3001");

socket.on('connected', (arg) => {
  console.log(arg);
})

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

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
