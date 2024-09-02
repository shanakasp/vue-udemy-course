<template>
  <h1>Child Component, Message from parent: {{ message }}</h1>
</template>

<script>
export default {
  name: "ChildComponent",
  props: {
    message: String,
  },
};
</script>

<style scoped>
h1 {
  color: red;
}
</style>
