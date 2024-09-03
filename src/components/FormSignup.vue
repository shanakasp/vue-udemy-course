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

  <label>Hobbies:</label>
  <br />
  <input type="checkbox" value="cricket" v-model="form.hobbies" /> Cricket
  <input type="checkbox" value="football" v-model="form.hobbies" /> Football
  <input type="checkbox" value="basketball" v-model="form.hobbies" /> Basketball
  <input type="checkbox" value="tennis" v-model="form.hobbies" /> Tennis

  <label>Select you gender</label>
  <select v-model="form.gender">
    <option value="male">Male</option>
    <option value="female">Female</option>
    <option value="other">Other</option>
  </select>

  <br /><br />
  <button v-on:click="login">Submit Login details</button>

  <br /><br />
  {{ form }}
</template>

<script>
export default {
  name: "FormSignup",
  data() {
    return {
      form: {
        username: "",
        password: "",
        hobbies: [],
        gender: [],
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
