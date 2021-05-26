<template>

 <LoginForm/>

</template>

<script>
import LoginForm from "./components/LoginForm"
export default {
  name: 'App',
  components: {
    LoginForm
    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  
}

* {
  box-sizing: border-box;
}
body {
  background-image: url("./assets/bg.jpg");
  background-position: center;
  background-repeat: no-repeat;
  }
</style>
