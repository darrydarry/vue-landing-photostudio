<template>
  <div class="block-wrap">
    <div class="img-line">
      <img :src="line" alt="line" />
    </div>

    <div class="block-first">
      <h3>Заявка</h3>
      <p>
        Съешь еще этих мягких французских булок, да выпей чаю. Съешь еще этих
        мягких.
      </p>
    </div>

    <div class="block-second">
      <h3>Бронь</h3>
      <p>
        Съешь еще этих мягких французских булок, да выпей чаю. Съешь еще этих
        мягких.
      </p>
    </div>

    <div class="block-third">
      <h3>Составление Технического задания</h3>
      <p>
        Съешь еще этих мягких французских булок, да выпей чаю. Съешь еще этих
        мягких.
      </p>
    </div>

    <div class="block-fourth">
      <h3>Съёмка</h3>
      <p>
        Съешь еще этих мягких французских булок, да выпей чаю. Съешь еще этих
        мягких.
      </p>
    </div>

    <div class="block-fifth">
      <h3>Готовые фото</h3>
      <p>
        Съешь еще этих мягких французских булок, да выпей чаю. Съешь еще этих
        мягких.
      </p>
    </div>
  </div>
</template>

<script>
import line from "../assets/img/line.svg";
export default {
  name: "WorkStages",
  data() {
    return {
      line,
    };
  },
};
</script>

<style lang="scss">
h2 {
  margin-top: 150px;
}
.block-wrap {
  position: relative;
  display: inline-block;
  margin: 100px;
}

.block-first h3,
.block-second h3,
.block-third h3,
.block-fourth h3,
.block-fifth h3 {
  font-weight: 600;
  font-size: 18px;
  line-height: 120%;
  color: #333333;
}

.block-third h3 {
  width: 219px;
}

.block-first p,
.block-second p,
.block-third p,
.block-fourth p,
.block-fifth p {
  font-size: 16px;
  line-height: 140%;
  color: #4a4a4a;
  margin-block-end: 0px;
  margin-block-start: 0px;
}

.block-first,
.block-second,
.block-third,
.block-fourth,
.block-fifth {
  background: #ffffff;
  border: 2px solid #e97522;
  box-shadow: 0px 24px 38px rgba(220, 220, 220, 0.14),
    0px 9px 46px rgba(216, 216, 216, 0.12),
    0px 11px 15px rgba(221, 221, 221, 0.2);
  border-radius: 12px;
  width: 269px;
  padding: 39px 39px 51px 40px;
}

.block-first {
  position: relative;
  top: 89px;
  left: 0px;
}

.block-second {
  position: relative;
  bottom: 87px;
  left: 694px;
}

.block-third {
  position: relative;
  top: 0;
  left: 760px;
}

.block-fourth {
  position: relative;

  bottom: 232px;
  left: 71px;
}

.block-fifth {
  position: relative;
  bottom: 153px;
  left: 441px;
}

.img-line {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 100px;
  left: 79px;
}

@media screen and (max-width: 1024px) and (min-width: 768px) {
  .block-wrap {
    margin: 0;
  }
  .img-line {
    left: -100px;
  }

  .block-first {
    top: 29px;
    left: 103px;
  }

  .block-second {
    bottom: 155px;
    left: 564px;
  }

  .block-third {
    left: 522px;
    top: -96px;
  }

  .block-fourth {
    bottom: 262px;
    left: 88px;
  }

  .block-fifth {
    bottom: 189px;
    left: 345px;
  }
}

@media screen and (max-width: 1268px) {
  .img-line {
    left: 29px;
  }
}
@media screen and (max-width: 1230px) {
  .block-third {
    left: 540px;
  }

  .block-second {
    left: 500px;
  }

  .img-line{
    left: 0;
  }
}
</style>