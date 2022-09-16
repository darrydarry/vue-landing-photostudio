<template>
  <div>
    <nav class="main-header">
      <div class="header-wrapp">
        <a href="/">
          <img :src="logo" alt="logo" class="logo" />
        </a>
        <div class="header-links-wrapp">
          <a
            v-for="(item, index) in itemsMenu"
            :key="index"
            href="/"
            class="header-link"
            >{{ item }}</a
          >
        </div>
        <div class="feedback">
          <button class="header-button">ОБРАТНЫЙ ЗВОНОК</button>
          <a class="phone-num" href="">+7 (499) 344 60 91</a>
        </div>

        <div class="icon-phone">
          <img :src="phone" alt="phone" />
        </div>

        <div class="icon-hamburger" @click="showMobileMenu">
          <img :src="hamburger" alt="hamburger" />
        </div>
      </div>
    </nav>

    <MobileMenu v-show="isShowMenu" :itemsMenu="itemsMenu" @hideMenu="isShowMenu = false" />
  </div>
</template>

<script>
import logo from "../assets/img/logo.png";
import phone from "../assets/img/phone.svg";
import hamburger from "../assets/img/hamburger.svg";
import MobileMenu from "./MobileMenu.vue";
export default {
  name: "HeaderComponent",
  components: {
    MobileMenu,
  },
  data() {
    return {
      logo,
      phone,
      hamburger,
      itemsMenu: [
        "Портфолио",
        "Виды работ",
        "О фотостудии",
        "Услуги и цены",
        "Контакты",
      ],
      isShowMenu: false,
    };
  },

  methods: {
    showMobileMenu() {
      this.isShowMenu = !this.isShowMenu;
    },

  },
};
</script>

<style lang="scss">
.main-header {
  position: fixed;
  margin: 0 auto;
  max-width: 1440px;
  width: 100%;
  left: 0;
  right: 0;
  z-index: 1006;

  .header-wrapp {
    display: flex;
    align-items: center;
    background-color: #ffffff;
    padding: 22px 100px;
    justify-content: space-between;

    .logo {
      width: 108px;
      height: 35px;
      margin-right: 32px;
    }

    .header-links-wrapp {
      display: flex;
    }
    .header-link {
      font-weight: 500;
      font-size: 14px;
      line-height: 20px;
      color: #4a4a4a;
      text-decoration: none;
      cursor: pointer;
      white-space: nowrap;
      margin-right: 32px;

      &:hover {
        color: #333333;
      }

      &:active {
        color: #e97522;
      }
    }
    .feedback {
      display: flex;
      align-items: center;
      flex-wrap: wrap;
    }
    .phone-num {
      font-weight: 600;
      font-size: 14px;
      line-height: 20px;
      margin-left: 24px;
      color: #585858;
      text-decoration: none;
    }

    .header-button {
      font-weight: 500;
      font-size: 12px;
      line-height: 15px;
      letter-spacing: 1px;
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
      }
    }
    .icon-hamburger,
    .icon-phone {
      display: none;
    }
  }

  // tablet styles
  @media screen and (max-width: 1024px) and (min-width: 768px) {
    width: 100%;
    margin: 0 auto;

    .header-wrapp {
      padding: 12px 80px;

      .icon-hamburger,
      .icon-phone {
        display: none;
      }

      .logo {
        width: 113px;
        height: 36px;
        margin-right: 24px;
      }

      .header-links-wrapp {
        flex-wrap: wrap;

        .header-link {
          font-size: 12px;
          margin-right: 24px;
        }
      }

      .feedback {
        flex-direction: column-reverse;
        align-items: flex-end;

        .phone-num {
          margin-bottom: 3px;
        }

        .header-button {
          font-size: 11px;
          line-height: 13px;
          width: 162px;
          padding: 8px 12px;
        }
      }
    }
  }

  // mobile styles
  @media screen and (max-width: 768px) {
    .header-wrapp {
      padding: 5px 16px;

      .icon-phone,
      .icon-hamburger {
        display: block;
      }

      .logo {
        width: 63px;
        height: 20px;
        margin-right: 24px;
      }

      .header-links-wrapp {
        display: none;

        .header-link {
          font-size: 12px;
          margin-right: 24px;
        }
      }

      .feedback {
        flex-direction: column-reverse;
        align-items: flex-end;

        .phone-num {
          margin-bottom: 3px;
        }

        .header-button {
          display: none;
        }
      }
    }
  }
}
</style>