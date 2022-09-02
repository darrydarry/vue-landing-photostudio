<template>
  <div>
    <HeaderComponent />
    <main class="main-container">
      <StudioDescription />
      <h2>Наши работы</h2>
      <SwiperComponent :photos="photoUrls" />
      <h2>Наши локации</h2>
      <SwiperComponent :photos="locationUrl" />
    </main>
  </div>
</template>

<script>
import HeaderComponent from "./HeaderComponent.vue";
import StudioDescription from "./StudioDescription.vue";
import SwiperComponent from "./SwiperComponent.vue";

import firstPhoto from "../assets/img/left.png";
import secondPhoto from "../assets/img/center.png";
import thirdPhoto from "../assets/img/right.png";

import street from "../assets/img/street.png";
import forest from "../assets/img/forest.png";
import house from "../assets/img/house.png";

export default {
  name: "LayoutPage",
  components: {
    HeaderComponent,
    StudioDescription,
    SwiperComponent,
  },
  data() {
    return {
      photoUrls: [
        firstPhoto,
        secondPhoto,
        thirdPhoto,
        secondPhoto,
        thirdPhoto,
        firstPhoto,
      ],
      locationUrl: [street, forest, house, forest, street],
    };
  },
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