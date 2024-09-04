<template>
  <div>
    <h1>Watchers in Vue</h1>
    <h2>{{ count }}</h2>
    <button v-on:click="increment">+</button>
    <button v-on:click="decrement">-</button>
  </div>
</template>

<script>
export default {
  name: "WatcherVue",
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      this.count--;
    },
  },

  watch: {
    count(newValue) {
      if (newValue > 10) {
        alert("Maximum count reached");
        this.count = 0;
      }
    },
  },
};
</script>

<style></style>
