<template>
  <div class="studio-description-container">
    <div class="studio-description-wrapp">
      <h1 class="studio-description-title">
        {{ title }}
      </h1>
      <h2 class="studio-description-subtitle">
        {{ subtitle }}
      </h2>
      <p class="studio-description-text">
        {{ text1 }}
      </p>
      <p class="studio-description-text">
        {{ text2 }}
      </p>
      <button class="button-consultation">
        {{ button }}
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "StudioDescription",
  data() {
    return {
      title: "Профессиональная фотосессия в студии",
      subtitle: "Наша фотостудия позволит исполнить ваши мечты",
      text1:
        "Фотографии стали неотъемлемой частью нашей жизни. Это теперь не просто памятные снимки в альбомах, ныне фото становиться способом понравиться окружающим, получить восхищение, заявить о себе всему миру.",
      text2:
        "Выбор правильной фотостудии занимает далеко не последнее место в получение фотографий. И мы с точностью заявляем, что нашей фотостудией вы останетесь довольны и еще не раз захотите возвращаться к нам.",
      button: "Получить консультацию",
    };
  },
};
</script>

<style lang="scss">
.studio-description-container {
  background-color: #444444;
}

.studio-description-wrapp {
  display: flex;
  flex-direction: column;
  padding: 149px 0 141px 100px;
  width: 791px;
  margin-bottom: 120px;
}

.studio-description-title {
  font: {
    weight: 700;
    size: 66px;
  }
  line-height: 78px;
  letter-spacing: 3.2px;
  color: #f5f5f5;
  margin: 0;
}

.studio-description-subtitle {
  font-weight: 600;
  font-size: 36px;
  line-height: 120%;
  color: #f5f5f5;
  width: 625px;

  @media screen and (max-width: 1024px) and (min-width: 768px) {
    font-size: 24px;
    line-height: 140%;
    width: 418px;
    text-align: unset;
  }
}

.studio-description-text {
  font-weight: 500;
  font-size: 16px;
  line-height: 26px;
  color: #f5f5f5;
  width: 653px;
  margin: 0;
}

.button-consultation {
  background: linear-gradient(180deg, #ffa96b -21.43%, #ee7a28 100%);
  border-radius: 10px;
  font-weight: 600;
  font-size: 16px;
  line-height: 20px;
  text-align: center;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: #ffffff;
  width: 366px;
  height: 64px;
  margin-top: 32px;
  cursor: pointer;
  transition: width 0.4s;

  &:hover {
    background: linear-gradient(180deg, #ffa96b 58.75%, #ee7a28 173.44%);
  }

  &:active {
    width: 319px;
    height: 56px;
    background: linear-gradient(180deg, #ffa96b 58.75%, #ee7a28 173.44%);
    font-size: 14px;
    line-height: 17px;
    letter-spacing: 2px;
  }
}

// tablet styles
@media screen and (max-width: 1024px) and (min-width: 768px) {
  .studio-description-wrapp {
    padding-left: 80px;
    padding-top: 70px;
    width: auto;

    .studio-description-title {
      width: 573px;
      font-size: 48px;
      line-height: 52px;
      letter-spacing: 2.3px;
    }

    .studio-description-subtitle {
      font-size: 24px;
      line-height: 140%;
      width: 418px;
      text-align: normal;
    }
  }
}

  // mobile styles
 @media screen and (max-width: 768px) {
  .studio-description-container {
    display: none;
  }
 }
</style>