<template>
  <input type="number" v-model="room_id">
  <input type="text" v-model="message">
  <button class="btn" @click="send">Отправить</button>
</template>

<script>
const {io} = require("socket.io-client");
// eslint-disable-next-line no-unused-vars
const socket = io("http://localhost:3001");

socket.on('massage',(data) => {
  console.log(data);
})

// socket.on('ping', (data) => {
//   console.log(data);
// })

export default {
  name: "ChatTest",
  data() {
    return {
      message: null,
      room_id: 1
    }
  },
  methods: {
    send() {
      socket.emit('message',{
      message: this.message,
        room_id: this.room_id
      });
    }
  }
}
</script>

<style scoped>

</style>