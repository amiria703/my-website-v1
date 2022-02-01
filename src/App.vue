<template>
  <div id="app">
    <div class="bg bg-purple"></div>
    <div class="bg bg-green"></div>
    <div class="bg bg-blue"></div>
    <header>
      <div class="logo">
        <img id="logo" src="./assets/images/logo.svg" alt="logo" />
      </div>
      <div class="title font-karla">The "Amiria703" Personal Website</div>
    </header>
    <div class="box">
      <div class="title bottom-line">About Me:</div>
      <p class="text">
        Hello Guys! I'm Amir Hossein Maher or in digital world, "amiria703"
        who's a 16 y.o. boy studying Math-Physics in 10th grade.
        <br />
        I'm a tech-lover who loves code and development; Also, I love one of the
        wonderful sutpid creature ever called Computer. Computers do as you
        command, I love this habit of them.
        <br />
        For now, I'm looking for a part/half time freelancing or Face-to-face
        job in Karaj, Alborz Province, Iran (It's where I live).
      </p>
    </div>
    <div class="box">
      <div class="title bottom-line">My Skills:</div>
      <div class="text">Here's some of skills I have in the technology world:</div>
      <div class="skill">HTML CSS JS:</div> 70%
    </div>
    <div class="box">
      <div class="title bottom-line">My Portfolios:</div>
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
/* Google Fonts: */
@import url("https://fonts.googleapis.com/css2?family=Karla:ital,wght@1,600&family=Titillium+Web:wght@300&display=swap");
/* 
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
} */
#app {
  direction: ltr;
  font-family: "Titillium Web", sans-serif;
}
.font-karla {
  font-family: "Karla", sans-serif;
}
#logo {
  width: 7rem;
  height: 7rem;
}
.logo {
  height: 7rem;
  margin-right: 10px;
}
header {
  padding: 0.5rem;
  display: flex;
  align-items: center;
}
.bg {
  width: 100%;
  height: 100%;
  position: fixed;
}
.bg-green {
  background: radial-gradient(
    circle,
    rgba(193, 255, 209, 1) 0%,
    rgba(255, 255, 255, 1) 60%
  );
  z-index: -999;
  width: 30%;
  height: 30%;
  left: 52%;
  top: 20%;
  opacity: 20%;
}
.bg-blue {
  background: radial-gradient(
    circle,
    rgb(94, 157, 216) 0%,
    rgba(255, 255, 255, 1) 40%
  );
  z-index: -999;
  width: 30%;
  height: 30%;
  opacity: 25%;
  left: 10%;
  top: 30%;
}
.bg-purple {
  background: radial-gradient(
    circle,
    rgba(126, 17, 173, 1) 0%,
    rgba(255, 255, 255, 1) 40%
  );
  z-index: -999;
  width: 40%;
  height: 40%;
  left: 25%;
  top: 50%;
  opacity: 30%;
}
.title {
  color: #7e11ad;
  font-size: 31pt;
}
.box {
  padding: 1rem;
  box-shadow: 0px 0px 8px -5px #000000;
  background: rgba(0, 0, 0, 0);
  border-radius: 1rem;
  margin: 1rem;
}
.text {
  margin: 1rem 0 0rem 0;
}
.bottom-line {
  padding-bottom: 0.5rem;
  border: solid #000;
  border-width: 0 0 1px 0;
}
</style>
