<template>
  <div class="overlay" :class="{active: isShow}"></div>
</template>

<script>
export default {
  name: "OverlayComponent",
  props: {
    isShow: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="scss">
.overlay {
    z-index: 1003;
    height: 100%;
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    display: none;

  &.active {
    background: rgba(15, 15, 15, 0.7);
    display: block;
  }
}
</style>