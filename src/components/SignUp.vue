<template>
  <img class="logo" src="../assets/logo.png"/>
  <h1>Sign up</h1>
  <div class="register">
    <input type="text" placeholder="Enter Name"/>
    <input type="email" placeholder="Enter Email"/>
    <input type="password" placeholder="Enter Password"/>
    <button>Sign Up</button>
  </div>
</template>

<script>
export default {
  name: "SignUp",
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
  width: 320px;
  height: 40px;
  border: 1px solid skyblue;
  border-radius: 5px;
  background-color: skyblue;
  color: white;
  cursor: pointer;
}
</style>