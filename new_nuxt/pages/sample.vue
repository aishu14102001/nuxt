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
  <div class="sample-page">
    <div class="container">
      <Header class="Header" />
      <div class="content">
        <div class="left-side">
          <div class="upper">
            <p>Boost Data Analysis with this tool, and see visible improvement in figures. </p>
          </div>
          <div class="lower">
            <p>Boost Data Analysis with this tool, and see visible improvement in figures.</p>
          </div>
        </div>

        <div class="right-side">
          <img src="../assets/Vector.png" alt="logo" style="max-width: 249px; max-height: 251px;">
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

.sample-page {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 95vh;
  margin: 0;
}

.container {
  border: 1px solid #ccc;
  border-radius: 40px;
  width: 100%;
  background: linear-gradient(127deg, #FFF 0.29%, rgba(255, 255, 255, 0.67) 31.2%, rgba(255, 255, 255, 0.33) 95.34%, rgba(255, 255, 255, 0.10) 116.12%, rgba(255, 255, 255, 0.00) 145.68%, rgba(255, 255, 255, 0.00) 174.9%);
  backdrop-filter: blur(69.60322570800781px);

}

.content {
  display: flex;
  flex-direction: row;
  overflow: hidden;
  width: 85%;
  height: 550px;
  border-radius: 20px;
}

.left-side {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 110px;
}

.right-side {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 20px;
}

.upper {
  width: 727px;
  font-family: Unbounded;
  font-size: 50px;
  font-weight: 400;
  line-height: 62px;
  text-align: left;
}

.lower {
  width: 727px;
  color: #222121;
  font-family: Open Sans;
  font-size: 30px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

img {
  max-width: 100%;
  height: auto;
}
</style>
<script>
import Header from "../components/Header.vue"
</script>
  