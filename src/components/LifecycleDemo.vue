<template>
  <div>
    <h1>Vue Lifecycle Demo</h1>
    <button @click="updateMessage">Update Message</button>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  name: "LifecycleDemo",
  data() {
    return {
      message: "Initial message",
    };
  },
  beforeCreate() {
    console.log(
      "beforeCreate: The instance is initialized but data not available."
    );
  },
  created() {
    console.log("created: Data has been set, but DOM not yet rendered.");
  },
  beforeMount() {
    console.log("beforeMount: The template is compiled but not mounted yet.");
  },
  mounted() {
    console.log("mounted: The component is now mounted on the DOM.");
  },
  beforeUpdate() {
    console.log("beforeUpdate: Data is about to change.");
  },
  updated() {
    console.log("updated: DOM has been re-rendered after data change.");
  },
  beforeUnmount() {
    console.log("beforeDestroy: Component is about to be destroyed.");
  },
  unmount() {
    console.log("destroyed: The component is now destroyed.");
  },
  methods: {
    updateMessage() {
      this.message = "Message updated!";
    },
  },
};
</script>

<style scoped>
/* Add some styling here if needed */
h1 {
  color: #42b983;
}
button {
  background-color: #42b983;
  color: white;
  padding: 10px 15px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
button:hover {
  background-color: #369f7e;
}
</style>
