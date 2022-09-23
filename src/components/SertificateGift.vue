<template>
  <div class="sertificate-gift-wrapp">
    <div class="sertificate-gift-left">
      <p class="sertificate-title">{{ title }}</p>
      <h3 class="sertificate-subtitle">{{ subtitle }}</h3>

      <div
        v-for="(item, index) in items"
        :key="index"
        class="sertificate-description-wrapp"
      >
        <img :src="item.img" alt="tick" />
        <p class="sertificate-title-description">{{ item.text }}</p>
      </div>
    </div>
    <div class="sertificate-gift-right">
      <img :src="envelope" alt="envelope" />
      <p class="sertificate-title-description-right">
        Срок действия сертификата: 2 месяца со дня приобретения.
      </p>
      <button class="sertificate-button">Приобрести</button>
    </div>
  </div>
</template>

<script>
import envelope from "../assets/img/envelope.png";
import tick from "../assets/img/tick.png";
export default {
  name: "SertificateGift",
  data() {
    return {
      envelope,
      title: "СЕРТИФИКАТ НА ФОТОСЕССИЮ",
      subtitle: "Это подарок, который западает в душу",
      items: [
        { text: "Креативное оформление", img: tick },
        { text: "Открытый календарь", img: tick },
        { text: "Всё включено", img: tick },
      ],
    };
  },
};
</script>

<style lang="scss">
.sertificate-gift-wrapp {
  display: flex;
  justify-content: space-evenly;
  background: #f2f4f4;
  border-radius: 25px;
  margin: 80px 80px;
  padding: 80px;

  .sertificate-title {
    font-size: 14px;
    line-height: 120%;
    letter-spacing: 1px;
    color: #c1c1c1;
    padding-top: 112px;
  }

  .sertificate-subtitle {
    font-size: 48px;
    width: 320px;
    line-height: 140%;
    letter-spacing: 1px;
    color: #4a4a4a;
    margin-top: 0;
  }

  .sertificate-title-description {
    font-size: 16px;
    line-height: 140%;
    color: #4a4a4a;
  }

  .sertificate-title-description-right {
    font-size: 16px;
    color: #4a4a4a;
  }

  .sertificate-button {
    width: 342px;
    height: 48px;
    background: linear-gradient(180deg, #ffa96b -21.43%, #ee7a28 100%);
    border-radius: 10px;
    font-size: 16px;
    line-height: 20px;
    text-align: center;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: #ffffff;
    border: none;
    cursor: pointer;
  }

  .sertificate-gift-left {
    width: 501px;
  }

  .sertificate-gift-right {
    text-align: center;
  }

  .sertificate-description-wrapp {
    display: flex;
    align-items: center;

    img {
      width: 24px;
      height: 24px;
      margin-right: 16px;
    }
  }
}

@media screen and (max-width: 1024px) and (min-width: 768px) {
  .sertificate-gift-wrapp {
    margin-right: 40px;
    margin-left: 40px;
    text-align: center;
    padding: 40px;
    justify-content: flex-start;

    .sertificate-button {
      width: 100%;
    }

    .sertificate-title{
      padding-top: 40px;
    }

    .sertificate-subtitle {
      font-size: 36px;
    }

    .sertificate-gift-right img {
      width: 100%;
    }

    .sertificate-gift-left {
      text-align: start;
    }

    .sertificate-title-description-right {
      margin-left: 39px;
      text-align: center;
    }
  }
}

@media screen and (max-width: 768px) {
  .sertificate-gift-wrapp {
    flex-direction: column;
    align-items: center;
    text-align: center;
    margin: 40px 16px;
    padding-bottom: 50px;

    .sertificate-title {
      font-size: 12px;
      padding-top: 40px;
    }

    .sertificate-subtitle {
      font-size: 24px;
      width: auto;
    }

    .sertificate-gift-left {
      width: initial;
    }

    .sertificate-gift-right img {
          width: 100%;
    }

    .sertificate-button {
      width: auto;
    }

    .sertificate-description-wrapp {
      display: block;

      img {
        margin-right: 0px;
      }
    }
  }
}
</style>