<template>
  <div class="container">
    <div class="heading-container">
      <div class="headers">
        <h1>My Stuff</h1>
        <h3>I build things. And like rockets.</h3>
      </div>
    </div>
    <Rocket />
    <SkillSet />
  </div>
</template>

<script>
import SkillSet from "@/components/SkillSet.vue";
import Rocket from "@/components/Rocket.vue";

export default {
  name: "about",
  components: {
    SkillSet,
    Rocket,
  },
};
</script>

<style scoped lang="scss">
h1 {
  @include heading-2;
  color: $white;
}

.container {
  width: 100%;
  color: $white;
}

.headers {
  text-align: left;
  display: inline-block;
  margin-top: 10%;
  margin-left: 25%;
}
</style>