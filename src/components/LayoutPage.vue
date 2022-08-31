<template>
  <div>
    <HeaderComponent />
    <main class="main-container">
      <div :style="{ height: '800px' }"></div>
    </main>
  </div>
</template>

<script>
import HeaderComponent from "./HeaderComponent.vue";
export default {
  name: "LayoutPage",
  components: { HeaderComponent },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Oswald&family=Quicksand&display=swap");
.main-container {
  max-width: 1440px;
  width: 100%;
  margin: 0 auto;
  font-family: "Montserrat";
  padding-top: 80px;
}
</style>