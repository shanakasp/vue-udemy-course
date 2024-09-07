<!-- src/views/Home.vue -->
<template>
  <div>
    <h1>Home Page</h1>
    <h2>Data from API</h2>

    <!-- Display fetched posts -->
    <ul>
      <li v-for="post in posts" :key="post.id">
        {{ post.title }} : {{ post.userId }}
      </li>
    </ul>

    <!-- Button to navigate to the About page -->
    <button @click="goToAbout">Go To About Page</button>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "HomePage",
  data() {
    return {
      posts: [],
    };
  },

  created() {
    this.fetchPosts();
  },

  methods: {
    goToAbout() {
      this.$router.push("/about");
    },
    async fetchPosts() {
      try {
        const response = await axios.get(
          "https://jsonplaceholder.typicode.com/posts"
        );
        this.posts = response.data;
        console.log(this.posts);
      } catch (error) {
        console.error("There was an error fetching the posts:", error);
      }
    },
  },
};
</script>

<style scoped>
button {
  margin-top: 20px;
  padding: 10px;
  background-color: #42b983;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
button:hover {
  background-color: #358a62;
}
</style>
