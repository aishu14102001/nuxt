<template>
  <div class="box">
    <div class="group">
      <div class="overlap-group">
        <div class="ellipse" />
        <div class="ellipse-1" />
        <div class="ellipse-2" />
        <div class="ellipse-3" />
        <div class="ellipse-4" />
        <div class="ellipse-5" />
      </div>
    </div>
  </div>
  <div class="password-page">
    <div class="container">
      <Header class="Header"/>
      <div class="content">
      <div class="left-side">
        <h2 class="password-title">Change Password</h2>
        <form @submit.prevent="resetPassword" class="form-group">
          
          <div class="input-container">
            <input :type="showPassword ? 'text' : 'password'" 
            id="password" 
            v-model="password" 
            placeholder="Password" 
            required/>
            <i @click="togglePasswordVisibility" :class="eyeIconClass">
              <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
            </i>
          </div><br>
          <div class="input-container">
            <input :type="showConfirmPassword ? 'text' : 'password'" 
            id="confirmpassword" 
            v-model="confirmpassword"
            placeholder="Confirm Password" required/>
            <i @click="togglePasswordConfirmVisibility" :class="eyeConfirmIconClass"></i>
          </div>
          <button type="submit" class="button">Submit</button>
        </form>
      </div>
      <div class="right-side">
        <div class="image-background"></div>
        <img src="@/assets/lock.png" alt="Image" style="max-height: 150px;"/>
      </div>
    </div>
    </div>
  </div>
</template>
  
<style scoped>
.box {
  height: 100%;
  width: 100%;
}

.group {
  height: 100%;
  left: 0;
  position: fixed;
  top: 0;
  width: 100%;
}

.overlap-group {
  height: 100%;
  position: relative;
}

.ellipse {
  background-color: #61cc6fa1;
  border-radius: 256.5px/426.62px;
  filter: blur(500px);
  height: 853px;
  left: 71px;
  position: absolute;
  top: 61px;
  width: 513px;
}

.ellipse-1 {
  background-color: #61cc6fa1;
  border-radius: 256.5px/426.62px;
  filter: blur(500px);
  height: 853px;
  left: 0;
  position: absolute;
  top: 798px;
  width: 513px;
}

.ellipse-2 {
  background-color: #61cc6fa1;
  border-radius: 256.5px/426.62px;
  filter: blur(500px);
  height: 853px;
  left: 1048px;
  position: absolute;
  top: 61px;
  width: 513px;
}

.ellipse-3 {
  background-color: #4c5f7e70;
  border-radius: 326.5px/477.78px;
  filter: blur(500px);
  height: 956px;
  left: 667px;
  position: absolute;
  top: 695px;
  width: 653px;
}

.ellipse-4 {
  background-color: #fdd93dad;
  border-radius: 289px/456.97px;
  filter: blur(500px);
  height: 914px;
  left: 240px;
  position: absolute;
  top: 695px;
  width: 578px;
}

.ellipse-5 {
  background-color: #fdd93dad;
  border-radius: 289px/456.97px;
  filter: blur(500px);
  height: 914px;
  left: 642px;
  position: absolute;
  top: 0;
  width: 578px;
}

.password-page {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 95vh;
  margin: 0;
}

.container {
  border: 1px solid #ccc;
  border-radius: 40px;
  width: 95%;
  background: linear-gradient(127deg, #FFF 0.29%, rgba(255, 255, 255, 0.67) 31.2%, rgba(255, 255, 255, 0.33) 95.34%, rgba(255, 255, 255, 0.10) 116.12%, rgba(255, 255, 255, 0.00) 145.68%, rgba(255, 255, 255, 0.00) 174.9%);
  backdrop-filter: blur(69.60322570800781px);

}

h2{
  font-style: normal;
}
.content{
  padding: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: 500px;
}
.left-side {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-style: normal;
  padding: 20px;
  font-weight: 400;
  font-family: 'Unbounded',sans-serif;
}

.right-side {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
}

h2 {
  text-align: center;
  margin-bottom: 50px;
}

input:focus {
  outline: #ccc;
}

input {
  background: transparent;
}

.input-container {
  position: relative;
}

input[type="password"],
input[type="confirm password"] {
  width: 300px;
  height: 35px;
  border: 1px solid #d0d0d0;
  border-radius: 5px;
}

input[type="text"] {
  width: 300px;
  height: 35px;
  border: 1px solid #d0d0d0;
  border-radius: 5px;
}

input[type="password"]::placeholder {
  color: #8f8d8d;
  padding-left: 25px;
  background-image: url('./assets/key.png');
  background-size: 16px 16px;
  background-repeat: no-repeat;
  background-position: 2% center;
}

input[type="confirmpassword"]::placeholder {
  color: #8f8d8d;
  padding-left: 25px;
  background-image: url('./assets/key.png');
  background-size: 16px 16px;
  background-repeat: no-repeat;
  background-position: 2% center;
}


.form-group {
  margin: 10px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 80px;
}

.button {
  font-family: 'Unbounded', sans-serif;
  font-size: 15px;
  background-color: #07aa53;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  width: 120px;
  height: 40px;
  margin: 25px;
}

img {
  max-width: 100%;
  height: auto;
  position: relative;
}

.image-background {
  position: absolute;
  width: 442.568px;
  height: 457.892px;
  flex-shrink: 0;
  border-radius: 457.892px;
  border: 0.903px solid #000;
  background: rgba(97, 204, 111, 0.30);
  filter: blur(130.25277709960938px);
}

i {
  position: absolute;
  top: 50%;
  size: 200px;
  right: 10px;
  transform: translateY(-50%);
  cursor: pointer;
  color: #8f8d8d;
}
</style>
  
<script>
import Header from "../components/Header.vue"
export default {
  data() {
    return {
      password: '',
      confirmpassword: '',
      showPassword: false,
      showConfirmPassword: false,
    };
  },
  methods: {
    resetPassword() {
      // Add your reset password logic here
      console.log('Resetting password for email:', this.password);
    },
    togglePasswordVisibility() {
      this.showPassword = !this.showPassword;
    },
    togglePasswordConfirmVisibility() {
      this.showConfirmPassword = !this.showConfirmPassword;
    },
  },
  computed: {
    eyeIconClass() {
      return this.showPassword ? 'fas fa-eye' : 'fas fa-eye-slash';
    },
    eyeConfirmIconClass() {
      return this.showConfirmPassword ? 'fas fa-eye' : 'fas fa-eye-slash';
    },
  },
};
</script>
  