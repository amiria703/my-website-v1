<template>
  <header>
    <div class="logo">
      <img id="logo" src="../assets/images/logo.svg" alt="logo" />
    </div>
    <div class="title font-karla">The "Amiria703" Personal Website</div>
  </header>
</template>

<script>
export default {
  name: "topHeader"
};
</script>

<style scoped>
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
</style>
