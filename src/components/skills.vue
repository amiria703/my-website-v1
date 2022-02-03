<template>
  <div>
    <div class="skills">
      <div class="margin-1" v-for="skill in skills" :key="skill">
        <div class="text-bigger">
          {{ skill.name }}:
          {{ skill.showPercent ? skill.showPercent : skill.percent + "%" }}
        </div>
        <div :class="'skill skill-' + skill.color">
          <div :class="'skill skill-' + skill.percent"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "topHeader",
  props: {
    skills: Array,
  },
};
</script>

<style scoped>
.skill {
  height: 1.5rem;
  width: 60%;
  border-radius: 2rem;
}
.skill-red {
  background: #640000;
}
.skill-red div {
  background: #e43838;
}
.skill-blue {
  background: #0b006d;
}
.skill-blue div {
  background: #686bff;
}
.skill-green {
  background: #00441a;
}
.skill-green div {
  background: #11fa6a;
}
.skill-90 {
  width: 90%;
}
.skill-50 {
  width: 50%;
}
</style>
