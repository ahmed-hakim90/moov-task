<template>
  <div id="app">
    <app-bar />
    <HeadAfterBar />
  </div>
</template>

<script>
import AppBar from "./components/AppBar.vue";
import HeadAfterBar from "./components/HeadAfterBar.vue";

export default {
  name: "App",
  components: {
    AppBar,
    HeadAfterBar
  }
};
</script>

<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  direction: rtl;
}
</style>
