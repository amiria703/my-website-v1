<template>
  <div id="app">
    <!-- Background blurred colors: -->
    <bg-blurred color="green"></bg-blurred>
    <bg-blurred color="blue"></bg-blurred>
    <bg-blurred color="purple"></bg-blurred>
    <!-- Top Header: -->
    <top-header />
    <!-- About: -->
    <box title="About Me">
      <p>
        Hello Guys! I'm Amir Hossein Maher or in the digital world, "amiria703"
        who's a 16 y.o. boy studying Math-Physics in 10th grade.
        <br />
        I'm a tech-lover who loves coding and development; Also, I love one of
        the most wonderful stupid creatures ever called Computer. Computers do
        as you command, I love this habit of them.
        <br />
        For now, I'm looking for a part-time/half-time in Karaj, Alborz
        Province, Iran or freelancing job.
      </p>
    </box>
    <!-- Skills: -->
    <box title="My Skills">
      <skills :skills="skills" />
    </box>
    <!-- Portfolios: -->
    <box title="My Portfolios">
      <portfolios :portfolios="portfolios"></portfolios>
    </box>
    <!-- Contact: -->
    <box title="Ways to Connect">
      <div class="links text-bigger">
        <span class="margin-1"
          >Telegram: <a href="https://t.me/amiria703">@amiria703</a></span
        >
        <span class="margin-1"
          >Email:
          <a href="mailto:amiria703@gmail.com">amiria703@gmail.com</a></span
        >
        <span class="margin-1"
          >Whatsapp:
          <a href="https://wa.me/+989229716813">+989229716813</a></span
        >
        <span class="margin-1"
          >Call & SMS: <a href="tel:+989229716813">+989229716813</a></span
        >
      </div>
    </box>
    <!-- Footer: -->
    <div class="footer">
      <div class="text-bigger">
        Made with ❤️ @ 🇮🇷 by VueJS and rendered using {{ browser }}
      </div>
    </div>
  </div>
</template>

<script>
import topHeader from "./components/topHeader";
import box from "./components/box";
import skills from "./components/skills";
import bgBlurred from "./components/bgBlurred";
import portfolios from "./components/portfolios";
export default {
  name: "App",
  components: {
    topHeader,
    box,
    skills,
    bgBlurred,
    portfolios,
  },
  data: () => {
    return {
      // All string,
      // name: name of skill,
      // percent: percent of skill,
      // color: color of skill bar,
      // showPercent: the percent which can be replaced with original percent in top part
      skills: [
        {
          name: "HTML",
          percent: "90",
          color: "red",
        },
        {
          name: "CSS",
          percent: "90",
          color: "blue",
        },
        {
          name: "JS",
          percent: "50",
          color: "red",
        },
        {
          name: "VueJS",
          percent: "50",
          color: "green",
        },
        {
          name: "C#",
          percent: "50",
          color: "blue",
        },
        {
          name: "English",
          percent: "50",
          showPercent: "C1",
          color: "green",
        },
      ],
      portfolios: [
        // name: name of portfolio,
        // image: name of image in @/assets/images
        // link: link to work website
        // githubLink: link to github of work
        {
          name: "My Own Website",
          image: "my-website.png",
          link: "https://amiria703.github.io",
          githubLink: "https://github.com/amiria703/my-website",
        },
      ],
    };
  },
  mounted: async () => {
    // Add animation of being hidden after 2500ms:
    await new Promise((r) => setTimeout(r, 2500));
    document.getElementById("white").classList.add("hidden");
    // Remove after 500ms:
    await new Promise((r) => setTimeout(r, 500));
    document.getElementById("white").remove();
  },
  computed: {
    // Detect browser based on user-agent for use in footer:
    browser: () => {
      if (
        (navigator.userAgent.indexOf("Opera") ||
          navigator.userAgent.indexOf("OPR")) != -1
      ) {
        return "Opera";
      } else if (navigator.userAgent.indexOf("Edg") != -1) {
        return "Microsoft Edge";
      } else if (navigator.userAgent.indexOf("Chrome") != -1) {
        return "Google Chrome";
      } else if (navigator.userAgent.indexOf("Safari") != -1) {
        return "Apple Safari";
      } else if (navigator.userAgent.indexOf("Firefox") != -1) {
        return "Mozilla Firefox";
      } else if (
        navigator.userAgent.indexOf("MSIE") != -1 ||
        !!document.documentMode == true
      ) {
        return "Internet Explorer";
      } else {
        return "a browser";
      }
    },
  },
};
</script>

<style>
/* Google Fonts: */
/* Fonts used: Karla & Titillium Web */
@import url("https://fonts.googleapis.com/css2?family=Karla:ital,wght@1,600&family=Titillium+Web:wght@300&display=swap");

* {
  cursor: default;
  user-select: none;
}
#app {
  direction: ltr;
  font-family: "Titillium Web", sans-serif;
}
.title {
  color: #7e11ad;
  font-size: xx-large;
}
.text-bigger {
  font-size: x-large;
}
a {
  font-style: italic;
  color: #6d7bff;
  cursor: pointer;
}
a:hover {
  color: #3649f7;
}
a img {
  cursor: pointer;
}
.font-karla {
  font-family: "Karla", sans-serif;
}
.margin-1 {
  margin: 1rem;
}

/* Other Styles: */

/* Contact Part: */
.links {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  justify-content: space-between;
}

/* Footer Part: */
.footer {
  text-align: center;
  background: #7e11ad;
  color: white;
  padding: 1rem;
}
</style>
