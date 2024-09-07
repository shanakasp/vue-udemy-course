<template>
  <div>
    <h1>Watchers in Vue</h1>
    <h2>{{ count }}</h2>
    <button v-on:click="increment">+</button>
    <button v-on:click="decrement">-</button>
    <ChildSlot data="Meta">
      <!-- Named slot for string -->
      <template v-slot:string>
        <p>This is a string passed to the string slot from the parent.</p>
      </template>

      <!-- Named slot for number -->
      <template v-slot:number>
        <p>{{ 42 }}</p>
      </template>

      <!-- Named slot for image -->
      <template v-slot:image>
        <img src="https://via.placeholder.com/150" alt="Sample Image" />
      </template>
    </ChildSlot>
    <LifecycleDemo />
  </div>
</template>

<script>
import ChildSlot from "./ChildSlot";
import LifecycleDemo from "./LifecycleDemo";
export default {
  name: "WatcherVue",
  components: {
    ChildSlot,
    LifecycleDemo,
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
