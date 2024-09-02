<template>
  <div>
    <h2>Child Component</h2>
    <p>Message from Parent: {{ parentData }}</p>
    <button @click="sendDataToParent">Send Data to Parent</button>
  </div>
</template>

<script>
export default {
  name: "ChildComponent",
  props: {
    parentData: String,
  },
  methods: {
    sendDataToParent() {
      this.$emit("childData", "Hello from Child!");
    },
  },
};
</script>
