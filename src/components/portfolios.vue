<template>
  <div class="portfolios text-bigger">
    <box class="portfolio" v-for="item in portfolios" :key="item">
      <a :href="item.link" target="_blank">
        <img
          :src="require(`@/assets/images/${item.image}`)"
          alt="portfolio-picture"
          class="portfolio"
      /></a>
      <div class="portfolio-text">
        <a :href="item.link" target="_blank">{{ item.name }}</a>
        <a :href="item.githubLink" target="_blank">
          <img
            src="@/assets/images/github.svg"
            alt="link to github"
            class="portfolio-github-img"
          />
        </a>
      </div>
    </box>
  </div>
</template>

<script>
import box from "./box";
export default {
  name: "portfolios",
  components: {
    box,
  },
  props: {
    portfolios: Array,
  },
};
</script>

<style scoped>
.portfolios {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
.portfolio {
  width: 100%;
  width: -moz-fill-available;
  width: -webkit-fill-available;
  width: fill-available;
  max-width: 25rem;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}
.portfolio-text {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  align-items: center;
}
.portfolio-github-img {
  width: 2rem;
  height: 2rem;
}
</style>
