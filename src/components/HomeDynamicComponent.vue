<template>
  <div>
    <h1>Home Dynamic Component</h1>

    <!-- Buttons to toggle between components -->
    <button @click="currentComponent = 'ComponentA'">Show Component A</button>
    <button @click="currentComponent = 'ComponentB'">Show Component B</button>

    <!-- Conditional rendering of components -->
    <ComponentA v-if="currentComponent === 'ComponentA'" />
    <ComponentB v-if="currentComponent === 'ComponentB'" />
  </div>
</template>

<script>
import ComponentA from "./ComponentA.vue";
import ComponentB from "./ComponentB.vue";

export default {
  name: "HomeDynamicComponent",
  components: {
    ComponentA,
    ComponentB,
  },
  data() {
    return {
      currentComponent: "ComponentA",
    };
  },
};
</script>

<style scoped>
button {
  margin: 10px;
}
</style>
