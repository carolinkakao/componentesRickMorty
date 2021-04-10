<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <NewComp  />
  </div>
</template>

<script>
import NewComp from "./components/NewComp.vue";

export default {
  name: "App",
  components: {
    NewComp,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
