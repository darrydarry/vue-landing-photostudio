
<template>
  <div class="swiper-main-container">
    <div class="wrap">
      <swiper class="swiper" :options="{...swiperOption, slidesPerView}">
        <swiper-slide v-for="(photoUrl, index) in photos" :key="index">
          <img :src="photoUrl" alt="photo" class="photo-img" />
        </swiper-slide>
      </swiper>
    </div>
    <div class="swiper-button-wrap"></div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css/swiper.css";

export default {
  name: "SwiperComponent",
  components: {
    Swiper,
    SwiperSlide,
  },
  props: {
    photos: {
      type: Array,
      default: null,
    },
    slidesPerView: {
      type: Number,
      default: 3,
    },
  },
  data() {
    return {
      swiperOption: {
        spaceBetween: 30,
      },
    };
  },
};
</script>

<style lang="scss">
.swiper-button-wrap,
.swiper-button {
  display: none;
}
.swiper-main-container {
  margin-bottom: 170px;
  @media screen and (max-width: 1024px) and (min-width: 768px) {
    margin-bottom: 0;
  }
}
h2 {
  font: {
    weight: 600;
    size: 36px;
  }
  line-height: 120%;
  text-align: center;
  color: #333333;
}
.photo-img {
  width: 100%;
  height: 100%;

  @media screen and (max-width: 1024px) and (min-width: 768px) {
    width: 367px;
    height: 362px;
  }
}
.wrap {
  display: flex;
  height: 500px;
}

// mobile styles
@media screen and (max-width: 768px) {
  .wrap {
    height: auto;
  }

  h2 {
    font-size: 24px;
    line-height: 140%;
  }

  .swiper-main-container {
    margin: 0;
  }

  .swiper-button-wrap {
    display: flex;
    justify-content: center;
    margin-top: 32px;
    margin-bottom: 60px;
  }

  .swiper-button {
    display: block;
    width: 320px;
    height: 56px;
    background: linear-gradient(180deg, #ffa96b -21.43%, #ee7a28 100%);
    border-radius: 10px;
    font-family: "Montserrat";
    font-weight: 600;
    font-size: 14px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: #ffffff;
    cursor: pointer;
    border: none;
  }

}
</style>