<template>
  <div class="mobile-header-links-wrap">
    <div class="header-menu-links">
      <a
        v-for="(item, index) in itemsMenu"
        :key="index"
        href="/"
        class="mobile-header-link"
      >
        {{ item }}
      </a>
    </div>

    <OverlayComponent isShow @click.native="$emit('hideMenu')" />
  </div>
</template>

<script>
import OverlayComponent from "./OverlayComponent.vue";

export default {
  name: "MobileMenu",
  components: {
    OverlayComponent,
  },
  props: {
    itemsMenu: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style lang="scss">
.mobile-header-links-wrap {
  width: 105px;
  position: fixed;
  z-index: 1004;
  top: 52px;
  right: 16px;

  .mobile-header-link {
    font-weight: 600;
    font-size: 14px;
    line-height: 20px;
    color: #ffffff;
    text-decoration: none;
    display: flex;
    justify-content: flex-end;
    margin-bottom: 16px;
  }
  
  .header-menu-links {
    position: relative;
    z-index: 9999999;
  }
}
</style>