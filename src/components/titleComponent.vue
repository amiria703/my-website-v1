<template>
  <div class="title bottom-line">{{ title }}:</div>
</template>

<script>
export default {
  name: "titleComponent",
  props: {
    title: String,
  },
};
</script>

<style scoped>
.bottom-line {
  padding-bottom: 0.5rem;
  border: solid #000;
  border-width: 0 0 1px 0;
  margin-bottom: 1rem;
}
</style>
