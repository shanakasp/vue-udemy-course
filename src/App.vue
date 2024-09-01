<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Shanaka Prince" />
    <PAGES />
    <TwoWayBinding />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import PAGES from "./components/PAGES.vue";
import TwoWayBinding from "./components/TwoWayBinding";

export default {
  name: "App",
  components: {
    HelloWorld,
    PAGES,
    TwoWayBinding,
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
