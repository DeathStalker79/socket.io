<template>
  <input type="text" v-model="message">
  <button class="btn" @click="send">Отправить</button>
</template>

<script>
const {io} = require("socket.io-client");
// eslint-disable-next-line no-unused-vars
const socket = io("http://localhost:3001");

export default {
  name: "ChatTest",
  data() {
    return {
      message: null
    }
  },
  methods: {
    send() {
      socket.emit('message', this.message);
    }
  }
}
</script>

<style scoped>

</style>