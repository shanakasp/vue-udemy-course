<!-- src/App.vue -->
<template>
  <div id="app">
    <nav>
      <!-- Navigation Links with custom classes -->

      <router-link to="/" class="nav-link">Home</router-link> |
      <router-link to="/about" class="nav-link">About</router-link>
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
/* Styling for the navigation and router links */
nav {
  margin-bottom: 20px;
}

.nav-link {
  margin-right: 10px;
  text-decoration: none;
  color: rgb(19, 204, 111);
  font-weight: bold;
}

.nav-link:hover {
  color: rgb(255, 102, 102); /* Change color on hover */
}
</style>
