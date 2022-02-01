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
        Hello Guys! I'm Amir Hossein Maher or in the digital world, "amiria703"
        who's a 16 y.o. boy studying Math-Physics in 10th grade.
        <br />
        I'm a tech-lover who loves coding and development; Also, I love one of
        the most wonderful stupid creatures ever called Computer. Computers do
        as you command, I love this habit of them.
        <br />
        For now, I'm looking for a part-time/half-time freelancing or
        Face-to-face job in Karaj, Alborz Province, Iran (It's where I live).
      </p>
    </div>
    <div class="box">
      <div class="title bottom-line">My Skills:</div>
      <div class="skill-text">HTML: 90%</div>
      <div class="skill-red">
        <div class="skill-90"></div>
      </div>
    </div>
    <div class="box">
      <div class="title bottom-line">My Portfolios:</div>
      <div class="portfolios">
        <div class="portfolio box">
          <img
            src="./assets/images/temp.jpg"
            alt="portfolio-picture"
            class="portfolio-img"
          />
          <div class="text">My Own Website</div>
        </div>
        <div class="portfolio box">
          <img
            src="./assets/images/temp.jpg"
            alt="portfolio-picture"
            class="portfolio-img"
          />
          <div class="text">My Own Website</div>
        </div>
        <div class="portfolio box">
          <img
            src="./assets/images/temp.jpg"
            alt="portfolio-picture"
            class="portfolio-img"
          />
          <div class="text">My Own Website</div>
        </div>
      </div>
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
  position: fixed;
  z-index: -999;
}
.bg-green {
  background: radial-gradient(
    circle,
    rgba(193, 255, 209, 1) 0%,
    rgba(255, 255, 255, 0) 60%
  );
  width: 30rem;
  height: 30rem;
  left: 52%;
  top: 10%;
  opacity: 20%;
}
.bg-blue {
  background: radial-gradient(
    circle,
    rgb(94, 157, 216) 0%,
    rgba(255, 255, 255, 0) 40%
  );
  width: 30rem;
  height: 30rem;
  opacity: 25%;
  left: 10%;
  top: 30%;
}
.bg-purple {
  background: radial-gradient(
    circle,
    rgba(126, 17, 173, 1) 0%,
    rgba(255, 255, 255, 0) 40%
  );
  width: 40rem;
  height: 40rem;
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
.bottom-line {
  padding-bottom: 0.5rem;
  border: solid #000;
  border-width: 0 0 1px 0;
  margin-bottom: 1rem;
}
.portfolios {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
.portfolio {
  width: -webkit-fill-available;
  max-width: 25rem;
}
.portfolio-img {
  width: -webkit-fill-available;
}
.skill-text {
  font-size: 20pt;
}
.skill-red {
  background: lightcoral;
  height: 1.5rem;
  width: 50%;
}
.skill-90 {
  width: 90%;
  background: red;
  height: 1.5rem;
}
</style>
