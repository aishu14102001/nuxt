<template>
  <div class="box">
    <div class="group">
      <div class="overlap-group">
        <div class="ellipse" />
        <div class="div" />
        <div class="ellipse-2" />
        <div class="ellipse-3" />
        <div class="ellipse-4" />
        <div class="ellipse-5" />
      </div>
    </div>
  </div>
  <div class="login-page">
    <div class="login-container">
      
      <Header class="Header" />
      
      <div class="content">
        <div class="login text-center">
          <h1 >Login</h1>

          <form @submit.prevent="login" class="login-form">
            <div class="form-group">
              <div class="input-container">
                <input type="phonenumber" id="phonenumber" v-model="phonenumber" placeholder="Enter registered phone number" required/>
              </div>
            </div>

            <div class="form-group">
              <div class="input-container">
                <input :type="showPassword ? 'password' : 'text'" id="password" v-model="password"
                required
                  placeholder="Password" />
                <i @click="togglePasswordVisibility" :class="eyeIconClass">
                  <link rel="stylesheet"
                    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
                </i>
              </div>
            </div>

            <div class="form-group">
              <div class="input-container align-forgot-password">
                <lable>
                  <!-- <input type="checkbox" id="check" v-model="checkbox" required/> -->
                  <a href="forgotPassword">Forgot Password?</a>
                </lable>
              </div>
            </div>
            <button type="submit" class="small-button">Login</button>
          </form>
        </div>

        <div class="sidebar">
          <!-- Image on the right side -->
          <img src="../assets/globe.png" alt="logo" style="max-width: 85%;" />
          <!-- Statement below the logo -->
          <div>
            <p>Transform Communication:</p>
            <p>Data-Driven Engagement,</p>
            <p>Streamlined Impact.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import Header from "../components/Header.vue"

export default {
  layout: 'default',
  data() {
    return {
      phonenumber: null,
      password: null,
      showPassword: true, // Initial value set to true
      loginError: null,
    };
  },
  computed: {
    eyeIconClass() {
      return this.showPassword ? "fas fa-eye-slash" : "fas fa-eye";
    },
  },

  methods: {
    login() {
      // Simulate a login request (replace with actual API call)
      if (this.phonenumber === "123456789" && this.password === "password123") {
        // Successful login
        this.loginError = null;
        console.log("Login successful");
        // Redirect or perform the desired action after successful login.
      } else {
        // Failed login
        this.loginError = "Invalid phonenumber or password. Please try again.";
        console.error("Login failed");
      }
    },
    togglePasswordVisibility() {
      this.showPassword = !this.showPassword;
    },
    toggleCheckbox() {
      this.checked = !this.checked;
    },

  },
};

</script>
<style scoped>
.box {
  height: 100%;
  width: 100%;
}

.box .group {
  height: 100%;
  left: 0;
  position: fixed;
  top: 0;
  width: 100%;
}

.box .overlap-group {
  height: 100%;
  position: relative;
}

.box .ellipse {
  background-color: #61cc6fa1;
  border-radius: 256.5px/426.62px;
  filter: blur(500px);
  height: 853px;
  left: 71px;
  position: absolute;
  top: 61px;
  width: 513px;
}

.box .div {
  background-color: #61cc6fa1;
  border-radius: 256.5px/426.62px;
  filter: blur(500px);
  height: 853px;
  left: 0;
  position: absolute;
  top: 798px;
  width: 513px;
}

.box .ellipse-2 {
  background-color: #61cc6fa1;
  border-radius: 256.5px/426.62px;
  filter: blur(500px);
  height: 853px;
  left: 1048px;
  position: absolute;
  top: 61px;
  width: 513px;
}

.box .ellipse-3 {
  background-color: #4c5f7e70;
  border-radius: 326.5px/477.78px;
  filter: blur(500px);
  height: 956px;
  left: 667px;
  position: absolute;
  top: 695px;
  width: 653px;
}

.box .ellipse-4 {
  background-color: #fdd93dad;
  border-radius: 289px/456.97px;
  filter: blur(500px);
  height: 914px;
  left: 240px;
  position: absolute;
  top: 695px;
  width: 578px;
}

.box .ellipse-5 {
  background-color: #fdd93dad;
  border-radius: 289px/456.97px;
  filter: blur(500px);
  height: 914px;
  left: 642px;
  position: absolute;
  top: 0;
  width: 578px;
}

input {
  background: transparent;
}

.input-container {
  position: relative;
}

h1{
  font-family: 'Unbounded', sans-serif; 
  font-style:normal;
  font-weight: 400;
  font-size: 36px;
}

.login-page {

  display: flex;
  justify-content: center;
  align-items: center;
  height: 95vh;
  margin: 0;
}

.login-container {

  border: 1px solid #ccc;
  border-radius: 40px;
  width: 95%;
  background: linear-gradient(127deg, #FFF 0.29%, rgba(255, 255, 255, 0.67) 31.2%, rgba(255, 255, 255, 0.33) 95.34%, rgba(255, 255, 255, 0.10) 116.12%, rgba(255, 255, 255, 0.00) 145.68%, rgba(255, 255, 255, 0.00) 174.9%);
  backdrop-filter: blur(69.60322570800781px);
}

.content {
  padding: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: 490px;
}


/* for moving the login form  */
.login {
  width: 60%;
  padding: 10px;
}

@media(max-width:700px) {
  .login text-center {
    flex-direction: column;
    align-items: center;
  }

}
.sidebar {
  width: 30%;
  padding: 10px;
  margin-right: 200px;
}
.sidebar > div {
  text-align: center;
  line-height: 1em; 
}

.sidebar>div p {
  font-size: 15px;
  font-family: 'Unbounded', sans-serif;
  color: #787b79;
  margin-right: 100px;
}

.login-form {
  display: flex;
  align-items: center;
  flex-direction: column;
}

@media(max-width: 800px) {

  .login-form {
    flex-direction: column;
    align-items: center;
  }
}

.form-group {
  margin: 10px;
  display: flex;
  flex-direction: column;
  height: 40px;

}

.input-container {
  display: flex;
  align-items: center;
  height: 50px;
  width: 300px;
}

@media(max-width: 900px) {
  .input-container {
    flex-direction: column;
    align-items: center;
  }
}

input:focus {
  outline: #ccc;
}

input[type="phonenumber"],
input[type="password"],
input[type="text"] {
  width: 100%;
  height: 35px;
  border: 1px solid #d0d0d0;
  border-radius: 5px;
}

input[type="phonenumber"]::placeholder {
  color: #8f8d8d;
  padding-left: 25px;
  background-image: url('./assets/dialpad.png');
  background-size: 16px 16px;
  background-repeat: no-repeat;
  background-position: 2% center;
}

input[type="password"]::placeholder {
  color: #8f8d8d;
  padding-left: 30px;
  background-image: url('./assets/key.png');
  background-size: 20px 16px;
  background-repeat: no-repeat;
  background-position: 2% center;

}

input[type="checkbox"] {
  margin-right: 20px;
  accent-color: rgb(212, 203, 203);
  border: black;
  border-color: black;

}

/* Define the small-button class for the smaller login button */
.small-button {
  background-color: #07aa53;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  width: 160px;
  height: 30px;
  margin: 25px;
}

button.small-button:hover {
  background-color: #07aa53;
}

a {
  text-decoration: none;
  color: #ff0004;
  cursor: pointer;
  margin-top: 10px;
}

a:hover {
  text-decoration: underline;
}

/* Additional styles for statement */


.text-center {
  text-align: center;
}

.align-forgot-password a {
  text-decoration: underline;
  color: #e94a57;
  margin-right: 125px;
  margin-top: 1px;
}

.align-forgot-password {
  display: flex;
  align-items: center;
  justify-content: flex-start;
}

.align-forgot-password input[type="checkbox"] {
  margin-right: 10px;
  justify-content: flex-start;
}


i {
  position: absolute;
  top: 50%;
  right: 10px;
  transform: translateY(-50%);
  cursor: pointer;
  color: #8f8d8d;
}</style>