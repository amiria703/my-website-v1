<template>
  <div id="app">
    <div class="image">
      <img id="profile" src="./assets/images/logo.png" alt="logo" />
    </div>
    <div class="texts">
      <div class="text">سلام! ✋ من امیرحسین ماهر هستم</div>
      <div class="text">برنامه‌نویس و طراح وب</div>
      <div class="text">در ادامه تعدادی از نمونه‌کارهای بنده رو مشاهده می‌کنید:</div>
    </div>
    <div class="portfolios">
      <div class="portfolio"></div>
    </div>
    <div class="links">
      <div class="link"><a href=""></a></div>
    </div>
    <div class="texts">
      <div class="text">
        این صفحه اینترنتی با VueJS ساخته و توسط {{ browser }} به نمایش درآمده است
      </div>
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
  mounted: async function(){
    await new Promise(r => setTimeout(r, 2000))
    document.getElementById("white").style.display = "none"
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
        return "مرورگر"
      }
    },
  },
};
</script>

<style>
@import "./assets/emoji/emoji.css";
</style>

<style>
.white {
  display: none;
}
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
.image #profile {
  width: 10rem;
  height: 10rem;
}
</style>
