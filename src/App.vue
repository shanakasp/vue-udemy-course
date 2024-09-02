<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Shanaka Prince" />
    <PAGES />
    <TwoWayBinding />
    <!-- Add the MultiInput component here -->
    <MultiInput />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import PAGES from "./components/PAGES.vue";
import TwoWayBinding from "./components/TwoWayBinding.vue"; // Make sure to include the .vue extension
import MultiInput from "./components/MultiInput.vue"; // Import the new component

export default {
  name: "App",
  components: {
    HelloWorld,
    PAGES,
    TwoWayBinding,
    MultiInput, // Register the new component
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
