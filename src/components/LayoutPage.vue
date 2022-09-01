<template>
  <div>
    <HeaderComponent />
    <main class="main-container">
      <StudioDescription />
    </main>
  </div>
</template>

<script>
import HeaderComponent from "./HeaderComponent.vue";
import StudioDescription from "./StudioDescription.vue";
export default {
  name: "LayoutPage",
  components: { HeaderComponent, StudioDescription },
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