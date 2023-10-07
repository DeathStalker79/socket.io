<template>
  <div class="home">
    <img src="../assets/logo.png" alt="Vue logo">
    <HelloWorld msg="Welcome to Your Vue.js APP"></HelloWorld>
    <input type="text">
    <button class="btn">Отправить</button>
  </div>
</template>

<script>
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  components: {
    HelloWorld
  }
}
</script>

<style scoped>

</style>