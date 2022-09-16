<template>
  <div class="price-cards-wrapp">
    <div v-for="(card, index) in cards" :key="index" class="card">
      <h4 class="card-title">{{ card.title }}</h4>

      <h1 class="price">{{ card.price }}</h1>

      <span class="price-info">{{ card.priceInfo }}</span>

      <p
        v-for="(description, i) in card.descriptions"
        :key="i"
        class="card-title-description"
      >
        <img :src="check" alt="check" /> {{ description }}
      </p>

      <h3 class="additional">{{ card.additionalTitle }}</h3>

      <div class="additional-wrapp">
        <span
          v-for="(addition, j) in card.additionals"
          :key="j"
          class="additional-description width-container"
        >
          {{ addition }}
        </span>
      </div>
      <center>
        <button class="button-price-cards">Забронировать</button>
      </center>
    </div>
  </div>
</template>

<script>
import check from "../assets/img/check-circle.png";
export default {
  name: "PriceComponent",

  data() {
    return {
      check,
      cards: [
        {
          title: "MINI",
          price: "2500 ₽",
          priceInfo: "/ 1 локация",
          descriptions: [
            "Длительность — 30 минут",
            "Исходники — До 100 штук",
            "Ретушь — 4 фото",
            "Аренда фотостудии — Бесплатно",
            "Любой образ",
          ],
          additionalTitle: "Дополнительные услуги",
          additionals: [
            "Помощь в позировании",
            "Визажист + 2000 ₽",
            "Дополнительная ретушь фото — 1 шт. / 250 ₽",
          ],
        },
        {
          title: "STANDART",
          price: "5000 ₽",
          priceInfo: "/ 2 локации",
          descriptions: [
            "Длительность — 1 час 20 минут",
            "Исходники — До 200 штук",
            "Ретушь — 8 фото",
            "Аренда фотостудии — Бесплатно",
            "Любой образ",
          ],
          additionalTitle: "Дополнительные услуги",
          additionals: [
            "Помощь в позировании",
            "Визажист + 2000 ₽",
            "Дополнительная ретушь фото — 1 шт. / 250 ₽",
          ],
        },
        {
          title: "MAXI",
          price: "N ₽",
          priceInfo: "/ Максимальное количество локаций",
          descriptions: [
            "Длительность — 4 часа",
            "Исходники — До 500 штук",
            "Ретушь — 50 фото",
            "Аренда фотостудии — Бесплатно",
            "Визажист — Make-Up, Укладка",
            "Предварительный подбор образов — До 8 образов",
          ],
          additionalTitle: "Дополнительные услуги",
          additionals: ["Дополнительная ретушь фото — 1 шт. / 250 ₽"],
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.card-title {
  font-size: 18px;
  line-height: 120%;
  color: #4a4a4a;
}

.card-title-description {
  font-weight: 500;
  font-size: 16px;
  line-height: 140%;
  color: #333333;
  display: flex;
  align-items: center;

  img {
    margin-right: 8px;
  }
}

.price {
  font-weight: 700;
  font-size: 56px;
  line-height: 120%;
  color: #333333;
  margin: 0px;
}

.price-info {
  font-weight: 600;
  font-size: 14px;
  line-height: 140%;
  color: #838383;
}

.additional {
  font-weight: 600;
  font-size: 16px;
  line-height: 140%;
  color: #333333;
  margin-top: 33px;
  text-align: center;
}

.additional-wrapp {
  display: flex;
  justify-content: space-evenly;
  text-align: center;
  margin-bottom: 50px;
}

.additional-description {
  font-weight: 500;
  font-size: 12px;
  line-height: 120%;
  color: #333333;
  height: 40px;
  margin-right: 5px;
  background: #ffffff;
  border: 1px solid #c2c2c2;
  border-radius: 5px;
  padding-top: 6px;
}

.card {
  background: #f2f4f4;
  border-radius: 16px;
  padding: 25px 13px 42px 20px;
  width: 380px;
  margin-right: 15px;
  margin-top: 34px;

  &:nth-child(2) {
    background: #f9f4ee;
  }

  &:nth-child(3) {
    background: #f5d9c6;
  }
}

.button-price-cards {
  width: 370px;
  height: 48px;
  background: linear-gradient(180deg, #ffa96b -21.43%, #ee7a28 100%);
  border-radius: 10px;
  font-weight: 600;
  font-size: 16px;
  line-height: 20px;
  text-align: center;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: #ffffff;
  border: none;
  cursor: pointer;
}

.price-cards-wrapp {
  display: flex;
  justify-content: center;
  margin-bottom: 160px;
  flex-wrap: wrap;
}

@media screen and (max-width: 768px) {
  .button-price-cards {
    width: 100%;
  }

  .card {
    width: 100%;
    margin: 0 0 20px 0;

  }

  .price-cards-wrapp {
    padding: 0 16px;
    margin-bottom: 40px;
  }

}
</style>