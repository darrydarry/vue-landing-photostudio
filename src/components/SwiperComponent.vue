
<template>
  <div class="swiper-main-container">
    <div class="wrap">
      <swiper class="swiper" :options="swiperOption">
        <swiper-slide v-for="(photoUrl, index) in photos" :key="index">
          <img :src="photoUrl" alt="photo" class="photo-img"/>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css/swiper.css";

export default {
  name: "SwiperComponent",
  title: "Auto slides per view / Carousel mode",
  components: {
    Swiper,
    SwiperSlide,
  },
  props: {
    photos: {
      type: Array,
      default: null,
    },
  },
  data() {
    return {
      swiperOption: {
        slidesPerView: 3,
        spaceBetween: 30,
      },
    };
  },
};
</script>

<style lang="scss">
.swiper-main-container {
  margin-top: 120px;
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
}
.wrap {
  display: flex;
  height: 500px;
}
</style>