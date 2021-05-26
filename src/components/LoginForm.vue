<template>
<div class="login">
    <h1>MY MILL</h1>
        <form>
            <label for="email">E-MAIL: </label>
            <input type="email" required placeholder="Enter email">
            <label for="password">PASSWORD: </label>

            <!-- I needed a container in order to position the image in the password input field -->
             <div id="password"> 
                 <!-- the colon enables JS (kinda like {} in JSX) -->
                 <!-- passwordIsVisible is a variable that returns a boolean value -->
                <input :type="passwordIsVisible? 'text': 'password'" required placeholder="Enter Password">
                <!-- store the oposite value in the variable on click -->
                <img src="/images/eye.svg" @click="passwordIsVisible = !passwordIsVisible"> 
            </div>
            

            <div class="inner-div"> 
                <p>Forgot password? 
                    <a href="https://www.google.com">Recover here</a>
                    <img src="/images/lock.svg">  
                </p>
                <input id="check" type="checkbox" required v-model="terms">
                <label>I agree to the TERMS AND CONDITIONS</label> 
            </div>

            <button>LOG IN</button>
        </form> 
</div>

</template>

<script>
  
export default {
  data () {
      return {
          terms: false, 
          passwordIsVisible: false, 
      }
  }
}
</script>

<style>

.login {
    background-color: white;
    text-align: left;
    max-width: 450px;
    margin: 50px auto; 
    padding: 40px; 
}

form {
    max-width: 380px;
    margin: 0 10%; 
    display: flex;
    justify-content: center;
    flex-direction: column;
}



.inner-div, button{
    margin: auto;
    text-align: center;
}

p {
      margin-bottom: 40px;
}

input, button {
     padding: 15px;
     border: none;
}

input:focus, button:focus {
    outline: none;
}

label, button {
    font-weight: bold;
    }

label {
    margin-bottom: 5px;
}

input {
    background-color: rgba(26, 26, 243, 0.034);
    border-bottom: 1.5px solid navy;
    margin-bottom: 20px;
}

.inner-div {
    font-size: 0.7em;
    margin-bottom: 10px;
}

.inner-div > p > img {
    margin: -3px; 
    margin-left: 5px;
}

button {
    background-color: navy;
    color: white;
    border-radius: 5px;
    width: 80%;
}

/* this is to add a custom styling to the checkbox */
#check {
    appearance:none; 
    background-color: white;
    border: 1px solid grey;
    border-radius: 2px;
    width: 15px;
    height: 15px;
    padding: unset; 
    margin: 0; 
    margin-right: 5px;
    outline: none;
}

#check:checked {
    background-color: navy;
    border: none; 
}

/* this is to position the eye (of the tiger) */
#password {
    position: relative; 
}

#password > input {
    width: 100%;
}

#password > img {
    position: absolute; 
    right: 0px; 
    bottom: 30px; 
    margin: unset;
}


</style>