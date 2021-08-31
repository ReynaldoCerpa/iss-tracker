<template>
  <div id="text">
    <h1>ISS Position</h1>
    <h2>Latitude: <span>{{ pos.iss_position.latitude }}</span> Longitude: <span>{{ pos.iss_position.longitude }}</span> </h2>
  </div>
</template>

<script>
export default {
  name: "Clock",
  data() {
    return {
      pos: 0,
    };
  },
  created() {
    setInterval(async () => {
      const response = await fetch("http://api.open-notify.org/iss-now.json");
      this.pos = await response.json();
      this.totalVuePackages = this.pos.total;
    }, 1000);
  },
};
</script>

<style>
  h1 {
    font-size: 2.4rem;
    margin-top: 5rem;
    margin-bottom: 0.5rem;
    
  }
  h2 {
    font-size: 2.5rem;
    height: 1rem;
    margin: 0;
  }
  span {
    color: #2ea8ff;
  }
</style>