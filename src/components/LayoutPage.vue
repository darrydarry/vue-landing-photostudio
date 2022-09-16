<template>
  <div>
    <HeaderComponent />
    <main class="main-container">
      <StudioDescription />

      <div>
        <h2>Наши работы</h2>
        <SwiperComponent :photos="photoUrls" />
      </div>

      <div>
        <h2>Наши локации</h2>
        <SwiperComponent
          :photos="locationUrl"
          class="visible-for-desktop-tablet"
        />

        <SwiperComponent
          :photos="locationUrl"
          class="visible-for-mobile"
          :slidesPerView="1"
        />
      </div>

      <div class="swiper-button-wrap">
        <button class="swiper-button">выбрать локацию</button>
      </div>

      <div>
        <h2>Виды услуг</h2>
        <ServisesComponent :images="servisesUrl" />
      </div>

      <h2>Этапы работ</h2>
      <!-- <WorkStages /> -->

      <DescriptionComponent />
      <h2>Стоимость фотосесии</h2>
      <PriceComponent />

      <DescriptionComponent2 />

      <h2>Подарочный сертификат на фотосессию</h2>
      <SertificateGift />

      <h2>Отзывы</h2>
      <FeedbackComponent />
    </main>
  </div>
</template>

<script>
import HeaderComponent from "./HeaderComponent.vue";
import StudioDescription from "./StudioDescription.vue";
import SwiperComponent from "./SwiperComponent.vue";
import ServisesComponent from "./ServisesComponent.vue";

// import WorkStages from "./WorkStages.vue"
import DescriptionComponent from "./DescriptionComponent.vue";
import PriceComponent from "./PriceComponent.vue";
import DescriptionComponent2 from "./DescriptionComponent2.vue";
import SertificateGift from "./SertificateGift.vue";
import FeedbackComponent from "./FeedbackComponent.vue";

import firstPhoto from "../assets/img/left.png";
import secondPhoto from "../assets/img/center.png";
import thirdPhoto from "../assets/img/right.png";

import street from "../assets/img/street.png";
import forest from "../assets/img/forest.png";
import house from "../assets/img/house.png";

import imgOne from "../assets/img/image1.png";
import imgTwo from "../assets/img/image2.png";
import imgThree from "../assets/img/image3.png";
import imgFour from "../assets/img/image4.png";
import imgFive from "../assets/img/image5.png";
import imgSix from "../assets/img/image6.png";
import imgSeven from "../assets/img/image7.png";
import imgEight from "../assets/img/image8.png";
import imgNine from "../assets/img/image9.png";
import imgTen from "../assets/img/image10.png";
import imgEleven from "../assets/img/image11.png";

export default {
  name: "LayoutPage",
  components: {
    HeaderComponent,
    StudioDescription,
    SwiperComponent,
    ServisesComponent,
    // WorkStages,
    DescriptionComponent,
    PriceComponent,
    DescriptionComponent2,
    SertificateGift,
    FeedbackComponent,
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
      servisesUrl: [
        { id: 1, src: imgOne, description: "Фотосессия Лав Стори" },
        { id: 2, src: imgTwo, description: "Фотосессия для парней" },
        { id: 3, src: imgThree, description: "Групповая фотосессия" },
        { id: 4, src: imgFour, description: "Фотосессия для беременных" },
        { id: 5, src: imgFive, description: "Фотосессия для подростков" },
        { id: 6, src: imgSix, description: "Фотосессия Лукбук" },
        { id: 7, src: imgSeven, description: "Фотосессия для девушек" },
        { id: 8, src: imgEight, description: "Фотосессия с животными" },
        { id: 9, src: imgNine, description: "Парная фотосессия" },
        { id: 10, src: imgTen, description: "Семейная фотосессия (дети +14)" },
        { id: 11, src: imgEleven, description: "Фотосессия «Деловой стиль»" },
      ],
    };
  },
};
</script>

<style lang="scss">
.main-container {
  max-width: 1440px;
  width: 100%;
  margin: 0 auto;
  padding-top: 80px;

  .visible-for-mobile {
    display: none;

    @media screen and (max-width: 768px) {
      display: block;
    }
  }

  .visible-for-desktop-tablet {
    display: none;

    @media screen and (min-width: 768px) {
      display: block;
    }
  }

  @media screen and (max-width: 1024px) and (min-width: 768px) {
    max-width: 1024px;
    width: 100%;
    margin: 0 auto;
  }
}
</style>