<template>
  <div>
    <div class="feedback-wrapp">
      <div v-for="(user, index) in users" :key="index" class="feedback-user">
        <img :src="user.src" alt="photo" />
        <h3 class="user-name">{{ user.name }}</h3>
        <p class="user-feedback">{{ user.feedback }}</p>
        <p class="full-feedback">Показать ещё</p>
      </div>
    </div>
    <div class="button-wrapp">
      <button class="button-feedback">Добавить отзыв</button>
    </div>
  </div>
</template>

<script>
import Mary from "../assets/img/Mary.png";
import Rus from "../assets/img/Rus.png";
import Serg from "../assets/img/Serg.png";

export default {
  name: "FeedbackComponent",

  data() {
    return {
      users: [
        {
          name: "Мария",
          src: Mary,
          feedback:
            "Съешь еще этих мягких французских булок, да выпей чаю. Съешь еще этих мягких французских булок, да выпей чаю. Съешь еще этих мягких французских булок, да выпей чаю.",
        },

        {
          name: "Сергей",
          src: Serg,
          feedback:
            "Съешь еще этих мягких французских булок, да выпей чаю. Съешь еще этих мягких французских булок, да выпей чаю. Съешь еще этих мягких французских булок, да выпей чаю.",
        },

        {
          name: "Руслан",
          src: Rus,
          feedback:
            "Съешь еще этих мягких французских булок, да выпей чаю. Съешь еще этих мягких французских булок, да выпей чаю. Съешь еще этих мягких французских булок, да выпей чаю.",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.feedback-wrapp {
  display: flex;
  padding: 100px 0;
  overflow-x: auto;
  justify-content: space-around;
}

.feedback-user {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 340px;
  min-width: 340px;
  padding: 10px;

  img {
    width: 210px;
    height: 230px;
  }
}

.user-name {
  font-weight: 600;
  font-size: 24px;
  line-height: 24px;
  color: #4a4a4a;
}
.user-feedback {
  font-size: 16px;
  line-height: 26px;
  text-align: center;
  color: #333333;
}

.full-feedback {
  cursor: pointer;
  font-size: 16px;
  line-height: 24px;
  text-align: center;
  color: #e97522;
}

.button-feedback {
  background: linear-gradient(180deg, #ffa96b -21.43%, #ee7a28 100%);
  border-radius: 10px;
  font-size: 16px;
  line-height: 20px;
  text-align: center;
  letter-spacing: 3px;
  text-transform: uppercase;
  color: #ffffff;
  width: 342px;
  height: 48px;
  border: none;
  cursor: pointer;
}

.button-wrapp {
  display: flex;
  justify-content: center;
}

@media screen and (max-width: 1024px) and (min-width: 768px) {
  .feedback-wrapp {
    justify-content: flex-start;
  }
}

@media screen and (max-width: 768px) {
  .feedback-wrapp {
    justify-content: flex-start;
  }
}
</style>