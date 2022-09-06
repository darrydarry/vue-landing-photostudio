<template>
  <div class="mobile-header-links-wrap">
    <a
      v-for="(item, index) in itemsMenu"
      :key="index"
      href="/"
      class="mobile-header-link"
    >
      {{ item }}
    </a>
  </div>
</template>

<script>
export default {
  name: "MobileMenu",
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
}
</style>