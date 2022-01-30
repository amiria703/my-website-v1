<template>
  <div id="app">
    <div class="bg"></div>
    <header>
      <div class="image">
        <img id="profile" src="./assets/images/logo.svg" alt="logo" />
      </div>
    </header>
    <div class="texts"></div>
    <div class="portfolios">
      <div class="portfolio"><img src="" alt="" class="" /></div>
    </div>
    <div class="links">
      <div class="link"><a href=""></a></div>
    </div>
    <div class="texts">
      <!-- <div class="text">
        این صفحه اینترنتی با VueJS ساخته و توسط {{ browser }} به نمایش درآمده
        است
      </div> -->
    </div>
  </div>
</template>

<script>
import "./assets/emoji/emoji.js";
export default {
  name: "App",
  components: {},
  data: function () {
    return {};
  },
  mounted: async function () {
    await new Promise((r) => setTimeout(r, 2500));
    document.getElementById("white").classList.add("hidden");
    await new Promise((r) => setTimeout(r, 500));
    document.getElementById("white").remove();
  },
  computed: {
    browser: function () {
      if (
        (navigator.userAgent.indexOf("Opera") ||
          navigator.userAgent.indexOf("OPR")) != -1
      ) {
        return "اُپِرا";
      } else if (navigator.userAgent.indexOf("Edg") != -1) {
        return "اِدج";
      } else if (navigator.userAgent.indexOf("Chrome") != -1) {
        return "کُروم";
      } else if (navigator.userAgent.indexOf("Safari") != -1) {
        return "سافاری";
      } else if (navigator.userAgent.indexOf("Firefox") != -1) {
        return "فایرفاکس";
      } else if (
        navigator.userAgent.indexOf("MSIE") != -1 ||
        !!document.documentMode == true
      ) {
        return "اینترنت اکسپلورر";
      } else {
        return "مرورگر";
      }
    },
  },
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
  font-family: Vazir;
}
#profile {
  width: 7rem;
  height: 7rem;
}
.image {
  height: 7rem;
}
header {
  margin-bottom: 0.5rem;
  /* background: #7e11ad; */
  padding: 0.5rem;
}
.bg {
  width: 100%;
  height: 100%;
  position: fixed;
}
.background {
  background: radial-gradient(
    circle,
    rgba(193, 255, 209, 1) 0%,
    rgba(255, 255, 255, 1) 100%
  );
  z-index: -999;
}
.white {
  z-index: -998;
}
</style>
