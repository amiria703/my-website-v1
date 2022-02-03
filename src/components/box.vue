<template>
  <div class="box">
    <title-component v-if="title" :title="title" />
    <slot />
  </div>
</template>

<script>
import titleComponent from "./titleComponent";
export default {
  name: "topHeader",
  components: {
      titleComponent
  },
  props: {
    title: String,
  },
};
</script>

<style scoped>
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
</style>
