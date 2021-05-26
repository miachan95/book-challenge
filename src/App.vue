<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/Book_community.png" width="25%" />
    <Decode challengeNum="1" />
  </div>
</template>

<script>
import Decode from "./components/Decode";

export default {
  name: "App",
  components: {
    Decode,
  },
  props: {
    challengeCode: String,
    challengeNum: String,
  },
};
</script>

<style>
html {
  background: #fff;
}
#app {
  font-family: "Source Code Pro", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #E18D96;
  margin-top: 60px;
}
</style>
