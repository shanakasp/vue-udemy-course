<!-- src/App.vue -->
<template>
  <div id="app">
    <nav>
      <!-- Navigation Links -->
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>

    <!-- Route View -->
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
/* Optional: Add some basic styling for the navigation */
nav {
  margin-bottom: 20px;
}
router-link {
  margin-right: 10px;
  text-decoration: none;
}
</style>
