<template >
    <div class="topnav">
    <div class="Header">
    <img src="../assets/Mannit_Logo_Light_Theme_Image_1.png" width="150" height="40" />

  <nav>
   <ul>
    <NuxtLink to="benefits" class="nav-item">
    <li>Benefits</li>
  </NuxtLink >
  <NuxtLink to="User guide" class="nav-item">
    <li >User Guide</li>
  </NuxtLink >
  <NuxtLink to ="Contact Us" class="nav-item">
    <li>Contact Us</li>
  </NuxtLink >
</ul>
</nav>

<div class="topnav">
  <button  class="install-button" @click="installApp" v-if="deferredPrompt">Get Mobile App</button>
  <!-- to navigate the login page  -->
  <nuxt-link to="/login">
<button type="submit" class="login-button">Login</button>
</nuxt-link>
<!-- to navigate the signup page -->
<nuxt-link to="/signup">
<button type="submit" class="signup-button">Signup</button>
</nuxt-link>
</div>
</div>
<!-- the nuxt link is used to render the current page -->
<nuxt/>
</div>
</template>


<style scoped>
.Header{
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  width:100%;
  margin-top: 30px;
}

ul{
    display: flex;
    gap: 110px;
}

.topnav{
display: flex;
gap: 5%;
}

.install-button {
  background-color:#6fe8f3;
  color: #070707;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  width: 170px;
  height: 30px;
  margin: 30px;
  margin-left: 60px;
  background-image: url(../assets/download.png);
  background-size: 16px 16px;
  background-repeat: no-repeat;
  background-position: 5% center;
  font-family: "Unbounded",sans-serif;
  font-size: 10px;
  padding-left:20px;
  
  }

.login-button{
background-color:#FFBC00;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  width: 120px;
  height: 30px;
  margin: 25px;
  margin-left: 60px;
}
.signup-button{
  background-color: #07aa53;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  width: 120px;
  height: 30px;
  margin: 25px;
}
.nav-item{
  list-style: none;
  text-decoration: none;
  color: #000;
  font-family: Open Sans;
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;  
}

@media screen and (max-width: 820px) {
  .Header {
    margin-top: 10px; /* Adjust the margin for smaller screens */
    flex-direction: column;
    text-align: center;
    align-items: center;
  }

  .Header img {
    width: 120px; /* Adjust the image size as needed */
    height: 32px; /* Adjust the image size as needed */
  }

  ul {
    align-items: center;
    flex-direction: column;
    gap: 10px; /* Adjust the gap between list items as needed */
  }

  .nav-item {
    font-size: 18px;
    align-items: center;
    margin: 0 10px;
  }

  .topnav {
    gap: 10px; /* Adjust the gap between elements in the topnav */
  }

  .login-button,
  .install-button,
  .signup-button {
    width: 100px; /* Adjust the button width as needed */
    height: 25px; /* Adjust the button height as needed */
    margin: 15px auto; /* Center the buttons horizontally and adjust the vertical margin as needed */
  }
}

@media screen and (max-width: 480px) {
  .Header img {
    width: 100px; /* Further adjust the image size for smaller screens */
    height: 26px; /* Further adjust the image size for smaller screens */
  }

  .nav-item {
    font-size: 16px;
    align-items: center;
  }
}

@media screen and(max-width: 1024px){
  .Header {
    margin-top: 10px; /* Adjust the margin for smaller screens */
    flex-direction: column;
    text-align: center;
    align-items: center;
  }

  .Header img {
    width: 120px; /* Adjust the image size as needed */
    height: 32px; /* Adjust the image size as needed */
  }

  ul {
    align-items: center;
    flex-direction: column;
    gap: 10px; /* Adjust the gap between list items as needed */
  }

  .nav-item {
    font-size: 18px;
    align-items: center;
    margin: 0 10px;
  }

  .topnav {
    gap: 10px; /* Adjust the gap between elements in the topnav */
  }

  .login-button,
  .install-button,
  .signup-button {
    width: 100px; /* Adjust the button width as needed */
    height: 25px; /* Adjust the button height as needed */
    margin: 15px auto; /* Center the buttons horizontally and adjust the vertical margin as needed */
  }
}
</style>

<script>
export default {
  data() {
    return {
      deferredPrompt: true,
    };
  },
  mounted() {
    window.addEventListener('beforeinstallprompt', (event) => {
      event.preventDefault();
      this.deferredPrompt = event;
    });
  },
  methods: {
    installApp() {
      if (this.deferredPrompt) {
        this.deferredPrompt.prompt();
        this.deferredPrompt.userChoice.then((choiceResult) => {
          if (choiceResult.outcome === 'accepted') {
            console.log('User accepted the install prompt');
          }
          this.deferredPrompt = false;
        });
      }
    },
  },
};
</script>
