<template>
  <div>
    <h1>Two-Way Data Binding Example</h1>

    <!-- Input bound to `message` -->
    <input v-model="message" placeholder="Type something..." />

    <!-- Display the bound data -->
    <p>You typed: {{ message }}</p>

    <!-- Select bound to `selectedOption` -->
    <select v-model="selectedOption">
      <option disabled value="">Please select an option</option>
      <option>Option 1</option>
      <option>Option 2</option>
      <option>Option 3</option>
    </select>

    <!-- Display the selected option -->
    <p>Selected option: {{ selectedOption }}</p>
  </div>
</template>

<script>
export default {
  name: "TwoWayBinding",

  data() {
    return {
      message: "", // For the text input
      selectedOption: "", // For the select dropdown
    };
  },
};
</script>

<style scoped>
/* Add your styles here */
</style>
