<template>
  <div id="nav">
    <router-link to="/">Home</router-link>
    <router-link to="/about">About</router-link>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" scoped>
#nav {
  padding: 30px;
  padding-right: 15%;
  text-align: right;

  a {
    font-weight: bold;
    color: $white;
    text-decoration: none;
    padding: 30px;
  }
}
</style>