<template>
  <img id="iss" alt="iss" src="./assets/iss.png" />
  <HelloWorld msg="Welcome to Your Vue.js App" />
  <Clock />
  <Input />
  <Timer />
</template>

<script>
import Clock from "./components/Clock.vue";

export default {
  name: "App",
  components: {
    Clock,
  },
};
</script>

<style>
html { 
  background: url("./assets/noche.gif");
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  margin-top: 60px;
}

#app{
  margin-top: 100px;
}

#iss {
  width: 50%;
  height: 65%;
}

img {
    position: relative;
    animation: bounce 2.5s infinite alternate;
    
  }
  @keyframes bounce {
      from {
          transform: translateY(0);
      }
      to {
          transform: translateY(1.7rem);
      }
  }
</style>