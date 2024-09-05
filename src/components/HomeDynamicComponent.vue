<template>
  <div>
    <h1>Home Dynamic Component</h1>

    <!-- Buttons to toggle between components -->
    <button @click="currentComponent = 'ComponentA'">Show Component A</button>
    <button @click="currentComponent = 'ComponentB'">Show Component B</button>

    <!-- Button to trigger notification -->
    <button @click="triggerNotification">Click to Notify</button>

    <!-- Conditional rendering of components -->
    <ComponentA v-if="currentComponent === 'ComponentA'" />
    <ComponentB v-if="currentComponent === 'ComponentB'" />

    <!-- AlertNotification Component -->
    <AlertNotification
      ref="alertNotification"
      message="Action Completed Successfully!"
    />
  </div>
</template>

<script>
import ComponentA from "./ComponentA.vue";
import ComponentB from "./ComponentB.vue";
import AlertNotification from "./AlertNotification.vue"; // Ensure this is the correct path and name

export default {
  name: "HomeDynamicComponent",
  components: {
    ComponentA,
    ComponentB,
    AlertNotification,
  },
  data() {
    return {
      currentComponent: "ComponentA",
    };
  },
  methods: {
    triggerNotification() {
      this.$refs.alertNotification.show();
    },
  },
};
</script>

<style scoped>
button {
  margin: 10px;
}
</style>
