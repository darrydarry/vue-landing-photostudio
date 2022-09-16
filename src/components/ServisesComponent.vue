<template>
  <div class="servises-image-wrap">
    <div
      v-for="servisesUrl in images"
      :key="servisesUrl.id"
      class="servises-image"
    >
      <img :src="servisesUrl.src" alt="image" />
      <div class="description">{{ servisesUrl.description }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ServisesComponent",
  props: {
    images: {
      type: Array,
      default: null,
    },
  },
};
</script>

<style lang="scss">
.servises-image-wrap {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  justify-items: center;
  grid-column-gap: 30px;
  grid-row-gap: 30px;
  padding-left: 100px;
  padding-right: 100px;
}

.servises-image img {
  width: 100%;
  height: 100%;
  border-radius: 15px;
}

.servises-image {
  position: relative;
}

.servises-image:nth-child(1) {
  grid-column-start: 1;
  grid-column-end: 1;
  grid-row-start: 1;
  grid-row-end: 1;
  width: 100%;
  height: 100%;
}

.servises-image:nth-child(2) {
  grid-column-start: 1;
  grid-column-end: 1;
  grid-row-start: 2;
  grid-row-end: 2;
  width: 100%;
  height: 100%;
}

.servises-image:nth-child(3) {
  grid-column-start: 1;
  grid-column-end: 1;
  grid-row-start: 3;
  grid-row-end: 5;
  width: 100%;
  height: 100%;
}

.servises-image:nth-child(4) {
  grid-column-start: 1;
  grid-column-end: 1;
  grid-row-start: 5;
  grid-row-end: 5;
  width: 100%;
  height: 100%;
}

.servises-image:nth-child(5) {
  grid-column-start: 2;
  grid-column-end: 2;
  grid-row-start: 1;
  grid-row-end: 3;
  width: 100%;
  height: 100%;
}

.servises-image:nth-child(6) {
  grid-column-start: 2;
  grid-column-end: 2;
  grid-row-start: 3;
  grid-row-end: 3;
  width: 100%;
  height: 100%;
}

.servises-image:nth-child(7) {
  grid-column-start: 2;
  grid-column-end: 4;
  grid-row-start: 4;
  grid-row-end: 4;
  width: 100%;
  height: 100%;
}

.servises-image:nth-child(8) {
  grid-column-start: 2;
  grid-column-end: 2;
  grid-row-start: 5;
  grid-row-end: 5;
  width: 100%;
  height: 100%;
}

.servises-image:nth-child(9) {
  grid-column-start: 3;
  grid-column-end: 3;
  grid-row-start: 1;
  grid-row-end: 1;
  width: 100%;
  height: 100%;
}

.servises-image:nth-child(10) {
  grid-column-start: 3;
  grid-column-end: 3;
  grid-row-start: 2;
  grid-row-end: 4;
  width: 100%;
  height: 100%;
}

.servises-image:nth-child(11) {
  grid-column-start: 3;
  grid-column-end: 3;
  grid-row-start: 5;
  grid-row-end: 5;
  width: 100%;
  height: 100%;
}

.description {
  font-weight: 600;
  font-size: 16px;
  line-height: 20px;
  color: #ffffff;
  position: absolute;
  bottom: 16px;
  left: 32px;
}

// tablet styles
@media screen and (max-width: 1024px) and (min-width: 768px) {
  h2 {
    font-size: 30px;
  }

  .description {
    bottom: 12px;
    left: 11px;
  }

  .servises-image-wrap {
    padding-left: 80px;
    padding-right: 80px;
  }
}

// mobile style
@media screen and (max-width: 768px) {
  .servises-image-wrap {
    grid-template-columns: 1fr 1fr;
    grid-column-gap: 16px;
    grid-row-gap: 18px;
    padding: 0;
  }

  .servises-image:nth-child(4) {
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 6;
    grid-row-end: 6;
  }

  .servises-image:nth-child(7) {
    grid-column-start: 2;
    grid-column-end: 2;
    grid-row-start: 7;
    grid-row-end: 7;
  }

  .servises-image:nth-child(8) {
    grid-column-start: 2;
    grid-column-end: 2;
    grid-row-start: 4;
    grid-row-end: 4;
  }

  .servises-image:nth-child(9) {
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 5;
    grid-row-end: 5;
  }

  .servises-image:nth-child(10) {
    grid-column-start: 2;
    grid-column-end: 2;
    grid-row-start: 5;
    grid-row-end: 7;
  }

  .servises-image:nth-child(11) {
    grid-column-start: 1;
    grid-column-end: 1;
    grid-row-start: 7;
    grid-row-end: 7;
  }

  .description {
    font-size: 14px;
    bottom: 8px;
    left: 12px;
  }
}
</style>