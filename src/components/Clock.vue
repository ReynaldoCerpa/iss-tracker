<template>
  <h2>The time is {{ hours }} : {{ minutes }}</h2>
</template>

<script>
export default {
  name: "Clock",
  data() {
    return {
      hours: 0,
      minutes: 0,
    };
  },
  created() {
    setInterval(() => {
      var date = new Date();
      this.hours = date.getHours();
      this.minutes = date.getMinutes();
    }, 1000);
  },
};
</script>
