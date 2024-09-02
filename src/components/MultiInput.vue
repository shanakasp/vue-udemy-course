<template>
  <div>
    <h1>Multi-Input Binding Example</h1>

    <!-- Input Field for Username -->
    <label>Username:</label>
    <input v-model="username" placeholder="Enter your username" />
    <p>Username: {{ username }}</p>

    <!-- Radio Buttons for Gender Selection -->
    <h2>Select Your Gender:</h2>
    <label><input type="radio" v-model="gender" value="Male" /> Male</label>
    <label><input type="radio" v-model="gender" value="Female" /> Female</label>
    <label><input type="radio" v-model="gender" value="Other" /> Other</label>
    <p>Selected Gender: {{ gender }}</p>

    <!-- Checkboxes for Hobbies Selection -->
    <h2>Select Your Hobbies:</h2>
    <label
      ><input type="checkbox" v-model="hobbies" value="Reading" />
      Reading</label
    >
    <label
      ><input type="checkbox" v-model="hobbies" value="Traveling" />
      Traveling</label
    >
    <label
      ><input type="checkbox" v-model="hobbies" value="Cooking" />
      Cooking</label
    >
    <label
      ><input type="checkbox" v-model="hobbies" value="Sports" /> Sports</label
    >
    <p>Selected Hobbies: {{ hobbies.join(", ") }}</p>
  </div>
</template>

<script>
export default {
  name: "MultiInput",
  data() {
    return {
      username: "",
      gender: "",
      hobbies: [],
    };
  },
};
</script>

<style scoped>
/* Add any styles specific to this component here */
h1,
h2 {
  color: #2c3e50;
}
label {
  margin-right: 10px;
}
</style>
