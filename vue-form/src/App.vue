<template>
  <!-- Event Bubbling -->
  <form v-on:submit.prevent="submitForm">
    <div>
      <label for="username">id: </label>
      <input type="text" name="username" id="username" v-model="username">
    </div>
    <div>
      <label for="password">password: </label>
      <input type="password" name="password" id="password" v-model="password">
    </div>
    <button type="submit">login</button>
  </form>
</template>

<script>
import axios from 'axios';

export default {
  data: function() {
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    submitForm: function() {
      // e.preventDefault();
      console.log(this.username, this.password);

      const url = 'https://jsonplaceholder.typicode.com/users';
      let data = {
        username: this.username,
        password: this.password,
      }
      axios
      .post(url, data)
      .then((res) => {
        console.log(res);
      })
      .catch((error) => {
        console.log(error)
      });
    },
  },
}
</script>

<style>

</style>