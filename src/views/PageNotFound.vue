<!-- src/views/PageNotFound.vue -->
<template>
  <div>
    <h1>404 - Page Not Found</h1>
    <p>The page you are looking for doesn't exist.</p>
    <router-link to="/">Go back to Home</router-link>
  </div>
</template>

<script>
export default {
  name: "PageNotFound",
};
</script>

<style>
/* Optional styles for the 404 page */
h1 {
  color: red;
}
</style>
