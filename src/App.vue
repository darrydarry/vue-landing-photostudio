<template>
  <div id="app">
    <layout-page />
  </div>
</template>

<script>
import LayoutPage from "./components/LayoutPage.vue";
export default {
  name: "App",
  components: {
    LayoutPage,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Oswald&family=Quicksand&display=swap");

body {
  margin: 0;
  font-family: "Montserrat";
}
</style>
