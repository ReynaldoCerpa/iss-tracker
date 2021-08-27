<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" />
  <Clock />
  <Input />
  <Timer />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Clock from "./components/Clock.vue";
import Timer from "./components/Timer.vue";
import Input from "./components/Input.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    Clock,
    Timer,
    Input,
  },
};
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
