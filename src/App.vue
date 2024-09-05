<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Shanaka Prince" />
    <PAGES />
    <TwoWayBinding />
    <MultiInput />
    <ConditionalRendering />
    <ForLoopArray />
    <FormSignup />
    <WatchersVue />
    <HomeDynamicComponent />
  </div>
</template>

<script>
import ConditionalRendering from "./components/ConditionalRendering.vue";
import ForLoopArray from "./components/ForLoopArray.vue";
import FormSignup from "./components/FormSignup.vue";
import HelloWorld from "./components/HelloWorld.vue";
import MultiInput from "./components/MultiInput.vue";
import PAGES from "./components/PAGES.vue";
import TwoWayBinding from "./components/TwoWayBinding.vue";
import WatchersVue from "./components/WatchersVue.vue";
import HomeDynamicComponent from "./components/HomeDynamicComponent";

export default {
  name: "App",
  components: {
    HelloWorld,
    PAGES,
    TwoWayBinding,
    ConditionalRendering,
    MultiInput,
    ForLoopArray,
    FormSignup,
    WatchersVue,
    HomeDynamicComponent,
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
