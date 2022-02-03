<template>
  <div :class="'bg bg-'+color"></div>
</template>

<script>
export default {
  name: "bgBlurred",
  props: {
    color: String,
  },
};
</script>

<style>
.bg {
  position: fixed;
  z-index: -999;
}
.bg-green {
  background: radial-gradient(
    circle,
    rgba(193, 255, 209, 1) 0%,
    rgba(255, 255, 255, 0) 40%
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
</style>
