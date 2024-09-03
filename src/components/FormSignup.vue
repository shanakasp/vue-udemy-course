<template>
  <h1 class="topic">Signup Form</h1>
  <label>
    User name:
    <input type="text" v-model="form.username" placeholder="Enter your name" />
  </label>

  <br /><br />

  <label>
    Password:
    <input
      type="password"
      v-model="form.password"
      placeholder="Enter your password"
    />
  </label>

  <button v-on:click="login">Submit Login details</button>
</template>

<script>
export default {
  name: "FormSignup",
  data() {
    return {
      form: {
        username: "",
        password: "",
      },
    };
  },
  methods: {
    login() {
      console.log("login data", this.form);
    },
  },
};
</script>

<style>
.topic {
  color: rgb(215, 20, 20);
  font-size: 25px;
  font-weight: bold;
  text-align: center;
  margin-top: 50px;
}
</style>
