<template>
  <div>
    <h1>Conditional Rendering Example</h1>

    <!-- v-if for checking a condition -->
    <p v-if="isLoggedIn">Welcome back, {{ username }}!</p>

    <!-- v-else-if for another condition -->
    <p v-else-if="hasAccount">You have an account. Please log in.</p>

    <!-- v-else for the default condition -->
    <p v-else>Welcome, Guest! Please sign up or log in.</p>

    <!-- Button to toggle login status -->
    <button @click="toggleLogin">Toggle Login Status</button>
  </div>
</template>

<script>
export default {
  name: "ConditionalRendering",
  data() {
    return {
      isLoggedIn: false,
      hasAccount: false,
      username: "Shanaka",
    };
  },
  methods: {
    toggleLogin() {
      this.isLoggedIn = !this.isLoggedIn;
    },
  },
};
</script>

<style scoped>
h1 {
  color: #2c3e50;
}
p {
  font-size: 18px;
  margin: 10px 0;
}
button {
  padding: 10px 20px;
  background-color: #42b983;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
button:hover {
  background-color: #349e76;
}
</style>
