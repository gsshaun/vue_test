<template>
  <div id="app">
    <button v-on:click="clickMe">Show</button>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "App",
  components: {},
  methods: {
    clickMe() {
      axios.get("https://api.npms.io/v2/search?q=vue").then((response) => {
        alert("Response From AXIOS GET: " + response.data.total);
        console.log("Response From AXIOS GET: ", response.data);
      });
    },
  },
};
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}
</style>
