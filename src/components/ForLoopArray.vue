<template>
  <div>
    <h1>List of Items</h1>

    <!-- Loop through the items array and render each item as a list -->
    <ul>
      <li v-for="(item, index) in items" :key="index">
        {{ index + 1 }}. {{ item.name }} - {{ item.price }}$
      </li>
    </ul>
    <ChildComponent
      :parentData="parentMessage"
      @childData="receiveDataFromChild"
    />
    <p>Message from Child: {{ dataFromChild }}</p>
  </div>
</template>

<script>
import ChildComponent from "./ChildComponent.vue";

export default {
  name: "ForLoopArray",
  components: {
    ChildComponent,
  },
  data() {
    return {
      items: [
        { name: "Apple", price: 1.99 },
        { name: "Banana", price: 0.99 },
        { name: "Cherry", price: 2.49 },
        { name: "Date", price: 3.0 },
        { name: "Elderberry", price: 1.5 },
      ],
      parentMessage: "Hello from Parent Component",
    };
  },
  methods: {
    receiveDataFromChild(data) {
      this.dataFromChild = data;
    },
  },
};
</script>

<style scoped>
h1 {
  color: #2c3e50;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  font-size: 18px;
  margin: 5px 0;
}
</style>
