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
body {
  margin: 0;
}
</style>
