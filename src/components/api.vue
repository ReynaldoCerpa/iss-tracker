<template>
  <h2>ISS Position: Latitude: {{ pos.iss_position.latitude }} longitude: {{ pos.iss_position.longitude }}</h2>
</template>

<script>
export default {
  name: "api",
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
