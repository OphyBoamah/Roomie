<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
</template>

<script>
export default {
  name: 'Nav',
};
</script>

<style scoped>
#nav {
  position: absolute;
  z-index: 100;
  width: 100%;
}
</style>
