<template>
  <form v-on:submit="submitForm">
    <div>
      <label for="username"> ID : </label>
      <input id="username" type="text" v-model="username">
    </div>
    <div>
      <label for="password"> PW: </label>
      <input id="password" type="password" v-model="password">
    </div>
    <button type="submit">LOGIN</button>
  </form>
</template>

<script>
import axios from 'axios';


export default {
  data: function() {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    submitForm: function(event) {
      event.preventDefault();
      console.log(this.username + " : " + this.password);
      var url = 'https://jsonplaceholder.typicode.com/users';
      var data= {
        username: this.username,
        password: this.password
      }
      axios.post(url, data)
        .then(function(response) {
          console.log(response);
        })
        .cathc(function(error){
          console.log(error);
        })
    }
    
  }
}
</script>

<style>

</style>