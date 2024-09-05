<template>
  <div>
    <h1>Watchers in Vue</h1>
    <h2>{{ count }}</h2>
    <button v-on:click="increment">+</button>
    <button v-on:click="decrement">-</button>
    <ChildSlot data="Meta">
      <p>
        This is content passed to the slot from the parent component.
      </p></ChildSlot
    >
  </div>
</template>

<script>
import ChildSlot from "./ChildSlot";
export default {
  name: "WatcherVue",
  components: {
    ChildSlot,
  },
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
