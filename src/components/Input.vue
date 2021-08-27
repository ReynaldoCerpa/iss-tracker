<template>
  <input type="text" v-model="inputText" />
  <p>Input text: {{ inputText }}.</p>
  <p v-show="flag">Don't say that!</p>
  
</template>

<script>
export default {
  name: "Input",
  data() {
    return {
      inputText: "",
      flag: false,
    };
  },
  watch: {
    inputText() {
      this.flag = this.inputText === "stupid";
      console.log("modified");
    },
  },
};
</script>
