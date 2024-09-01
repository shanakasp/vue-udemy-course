<template>
  <div>
    <h1 class="h1">Hello Shanaka {{ email }}</h1>
    <h2>{{ number }}</h2>
    <h3>{{ getName(111) }}</h3>
    <h3>User Data: {{ getData() }}</h3>
    <h3>{{ getData().email }}</h3>
    <h3>{{ getData().phoneNumber }}</h3>
    <button @click="handleClick">Click Here</button>
    <button v-on="{ click: handleClick }">submit</button>
  </div>
</template>

<script>
export default {
  name: "PAGES",

  data() {
    return {
      email: "shanakaprince@gmail.com",
      number: "22222",
    };
  },

  methods: {
    getName(a) {
      return a;
    },
    getData() {
      return {
        email: "abc@gmail.com",
        phoneNumber: 123456,
      };
    },
    handleClick() {
      console.log("handleClick 123");
    },
  },
};
</script>

<style scoped>
.h1 {
  color: blueviolet;
}
</style>
