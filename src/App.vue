<template>
  <div id="app">
    <div class="image">
      <img id="profile" src="" alt="" />
    </div>
    <div class="texts">
      <div id="text">سلام! ✋ من امیرحسین ماهر هستم.</div>
    </div>
    <div class="portfolios">
      <div class="portfolio"></div>
    </div>
    <div class="links">
      <div class="link"></div>
    </div>
  </div>
</template>

<script>
import "./assets/emoji/emoji.js";
export default {
  name: "App",
  components: {},
};
</script>

<style>
@import "./assets/emoji/emoji.css";
</style>

<style>
@font-face {
  font-family: Vazir;
  src: url("./assets/fonts/Vazir-Regular.eot");
  src: url("./assets/fonts/Vazir-Regular.eot?#iefix")
      format("embedded-opentype"),
    url("./assets/fonts/Vazir-Regular.woff2") format("woff2"),
    url("./assets/fonts/Vazir-Regular.woff") format("woff"),
    url("./assets/fonts/Vazir-Regular.ttf") format("truetype");
  font-weight: normal;
  font-style: normal;
}
#app {
  direction: rtl;
  text-align: center;
  font-family: Vazir;
}
</style>
