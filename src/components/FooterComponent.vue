<template>
  <div class="footer-wrapp">
    <div class="footer-links-menu">
      <div class="footer-logo">
        <img :src="logo" alt="logo" class="logo" />
      </div>

      <div class="footer-links-wrapp">
        <a
          v-for="(item, index) in footerMenu"
          :key="index"
          href="/"
          class="footer-link"
          >{{ item }}</a
        >
      </div>
    </div>

    <div class="line"></div>

    <div class="social-logos-menu">
      <div>
        <span class="socail-text">Наши социальные сети:</span>
      </div>
      <div class="social-img-wrapp">
        <img
          v-for="(link, i) in social"
          :key="i"
          :src="link"
          alt="social"
          class="social-img"
        />
      </div>
    </div>
  </div>
</template>

<script>
import logo from "../assets/img/logo.png";

import inst from "../assets/img/inst.svg";
import fb from "../assets/img/fb.svg";
import tw from "../assets/img/tw.svg";
import tg from "../assets/img/tg.svg";

export default {
  name: "FooterComponent",

  data() {
    return {
      logo,
      footerMenu: [
        "Портфолио",
        "Виды работ",
        "О фотостудии",
        "Услуги и цены",
        "Отзывы",
        "Контакты",
      ],
      social: [inst, fb, tw, tg],
    };
  },
};
</script>

<style lang="scss">
.footer-wrapp {
  background: #f2f4f4;
  margin-top: 150px;

  .footer-links-menu {
    display: flex;
    padding: 60px 100px 32px;
    justify-content: space-around;
  }

  .logo {
    width: 185px;
    height: 55px;
  }

  .footer-links-wrapp {
    display: flex;
    flex-wrap: wrap;
  }

  .footer-link {
    text-decoration: none;
    font-size: 16px;
    line-height: 26px;
    color: #4a4a4a;
    justify-content: space-around;
    display: flex;
    align-items: flex-end;
    white-space: nowrap;
    padding-right: 15px;

    &:hover {
      color: #333333;
    }

    &:active {
      color: #e97522;
    }
  }

  .line {
    border: 1px solid #b1b1b1;
    margin: 0px 100px;
  }

  .socail-text {
    font-size: 16px;
    line-height: 28px;
    color: #333333;
    white-space: nowrap;
  }

  .social-logos-menu {
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 30px;
    padding-bottom: 60px;
  }

  .social-img {
    padding-left: 20px;
    padding-right: 10px;
    cursor: pointer;
  }
}

@media screen and (max-width: 1024px) and (min-width: 768px) {
  .footer-wrapp {
    .logo {
      width: 212px;
    }

    .footer-links-menu {
      padding: 56px 80px 32px;
    }

    .footer-links-wrapp {
      padding-left: 160px;
      justify-content: flex-end;
    }

    .footer-link {
      padding-right: 60px;
    }

    .line {
      margin: 0px 80px;
    }
  }
}

@media screen and (max-width: 768px) {
  .footer-wrapp {
    .footer-links-wrapp {
      padding-top: 51px;
      justify-content: center;
    }

    .footer-links-menu {
      flex-direction: column;
      padding: 52px 61px 32px;
    }
    .social-logos-menu {
      flex-direction: column;
      padding: 40px 80px;
      align-items: center;
    }

    .social-img-wrapp {
      padding-top: 16px;
    }

    .social-img {
      padding-right: 0px;
    }

    .footer-logo {
      display: flex;
      justify-content: center;
    }
  }
}
</style>