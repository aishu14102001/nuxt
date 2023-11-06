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
    <div class="forgotPassword-page">
        <div class="container">
            <Header class="Header" />
            <div class="content">
            <div class="left-side">
                <h2>Forgot Password?</h2><br><br>
                <form @submit.prevent="resetPassword" class="form-group">
                    <div class="input-container">
                        <input type="phonenumber" id="phonenumber" v-model="phonenumber" placeholder="Enter registered phone number" required/>
                    </div><br>
                    <button type="submit" class="button">Send OTP</button>
                </form>
            </div>
            <div class="right-side">
                <div class="image-background"></div>
                <img src="@/assets/forgot.png" alt="Image" style="max-height: 150px;" />
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

.box .ellipse-1 {
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


.forgotPassword-page {
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

.content{
    padding: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
    height: 500px;
}
.left-side {
    font-family: 'Unbounded',sans-serif;
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 20px;
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
    margin-bottom: 20px;
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

input[type="phonenumber"] {
    width: 300px;
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

.form-group {
    margin: 10px 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    /* Center the input field and button horizontally */
    justify-content: center;
    /* Center the input field and button vertically */
    height: 80px;
    /* Increase the height to accommodate the input and button */
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
    /* Adjust the width to your desired size */
    height: 40px;
    /* Adjust the height to your desired size */
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
    background: rgba(253, 217, 61, 0.30);
    filter: blur(104.24223327636719px);
}

@media (max-width: 480px) {
  /* Add your styles for screens with a maximum width of 480px */
  h2 {
    font-size: 20px;
  }

  input[type="phonenumber"] {
    width: 100%;
  }

  .button {
    width: 100%;
  }
}

@media (max-width: 320px) {
  /* Add your styles for screens with a maximum width of 320px */
  h2 {
    font-size: 18px;
  }

  input[type="phonenumber"] {
    width: 100%;
  }

  .button {
    width: 100%;
  }
}
@media (max-width: 768px) {
  /* Add your responsive styles for screens with a maximum width of 768px */
  .container {
    width: 90%;
    /* Adjust container width for smaller screens */
  }

  .content {
    height: auto;
    flex-direction: column;
    padding: 20px;
  }

  .left-side {
    padding: 10px;
    text-align: center;
  }

  .right-side {
    padding: 10px;
  }

  h2 {
    font-size: 24px;
  }

  input[type="phonenumber"] {
    width: 100%;
  }

  .button {
    width: 100%;
  }

  img {
    max-width: 100%;
    height: auto;
  }

  .image-background {
    width: 100%;
    height: auto;
  }
}
</style>
  
<script>
import Header from "../components/Header.vue"
export default {
    data() {
        return {
            phonenumber: '',
        };
    },
    methods: {
        resetPassword() {
            // Add your reset password logic here
            console.log('Resetting password for phonenumber:', this.phonenumber);
        },
    },
};
</script>