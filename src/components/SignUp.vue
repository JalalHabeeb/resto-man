<template>
  <img class="logo" src="../assets/logo.png"/>
  <h1>Sign up</h1>
  <div class="register">
    <input type="text" v-model="name" placeholder="Enter Name"/>
    <input type="email" v-model="email" placeholder="Enter Email"/>
    <input type="password" v-model="password" placeholder="Enter Password"/>
    <button v-on:click="signUp">Sign Up</button>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: "SignUp",
  data() {
    return {
      name: '',
      email: '',
      password: ''
    }
  },
  methods: {
    async signUp() {
      let result = await axios.post('http://localhost:3000/users',{
        email: this.email,
        password: this.password,
        name: this.name
      });

      console.warn(result)
      if(result.status === 201) {
        localStorage.setItem('user-info', JSON.stringify(result.data))
        this.$router.push({name: "HomePage"})
      }
    }
  }
};
</script>

<style>
.logo{
  width: 100px;
}

.register input {
  width: 300 px;
  height: 40px;
  padding-left: 20px;
  display: block;
  margin: auto auto 30px auto;
  border: 1px solid skyblue;
  border-radius: 5px;
}

.register button {
  width: 300px;
  height: 40px;
  border: 1px solid skyblue;
  border-radius: 5px;
  background-color: skyblue;
  color: white;
  cursor: pointer;
}
</style>