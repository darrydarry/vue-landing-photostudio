<template>
  <nav>
    <div class="header-wrapp">
      <a>
        <img :src="logo" alt="logo" />
      </a>
      <div class="header-links-wrapp">
        <a v-for="(item, index) in itemsMenu" :key="index" href="">{{
          item
        }}</a>
      </div>
      <div class="feedback">
        <button class="header-button">ОБРАТНЫЙ ЗВОНОК</button>
        <a class="phone-num" href="">+7 (499) 344 60 91</a>
      </div>
    </div>
  </nav>
</template>

<script>
import logo from "../assets/img/logo.png";
export default {
  name: "HeaderComponent",
  data() {
    return {
      logo,
      itemsMenu: [
        "Портфолио",
        "Виды работ",
        "О фотостудии",
        "Услуги и цены",
        "Контакты",
      ],
    };
  },
};
</script>

<style lang="scss">
nav {
  position: fixed;
  margin: 0 auto;
  max-width: 1440px;
  width: 100%;
  left: 0;
  right: 0;
  z-index: 1000;
}
.header-wrapp {
  display: flex;
  align-items: center;
  background-color: #ffffff;
  padding-left: 100px;
  padding-right: 100px;

  .header-links-wrapp {
    padding: 30px 102px;
    width: 581px;
    display: flex;
  }
  a {
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 20px;
    color: #4a4a4a;
    text-decoration: none;
    cursor: pointer;
    text-indent: 30px;

    &:hover {
      font-weight: 500;
      font-size: 14px;
      line-height: 20px;
      color: #333333;
    }

    &:active {
      font-weight: 500;
      font-size: 14px;
      color: #e97522;
    }
  }
  .feedback {
    width: 348px;
    display: flex;
    align-items: center;
  }
  .phone-num {
    font-weight: 600;
    font-size: 14px;
    line-height: 20px;
  }
  img {
    width: 108px;
    height: 35px;
  }
  button {
    width: 196px;
    height: 31px;
    font-style: normal;
    font-weight: 500;
    font-size: 12px;
    line-height: 15px;
    color: #e97522;
    border: 2px solid #e97522;
    border-radius: 10px;
    background-color: #ffffff;
    cursor: pointer;
    padding: 8px 24px;
    transition: width 0.1s;

    &:hover {
      background: #e97522;
      color: #ffffff;
    }

    &:active {
      width: 173px;
      height: 28px;
      font-size: 10px;
      line-height: 12px;
      letter-spacing: 1px;
      color: #ffffff;
      background: #e97522;
    }
  }
}
</style>