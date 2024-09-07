<!-- src/views/Home.vue -->
<template>
  <div>
    <h1>Home Page</h1>
  </div>

  <button @click="goToAbout">Go To About Page</button>
</template>

<script>
export default {
  name: "HomePage",

  methods: {
    goToAbout() {
      this.$router.push("/about");
    },
  },
};
</script>
