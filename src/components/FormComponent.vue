<template>
  <div class="form-main-container">
    <div class="form-wrapp">
      <h3 class="form-title">Форма обратной связи</h3>

      <span class="input-title">Имя</span>
      <input type="text" placeholder="Введите ваше имя" class="input" />

      <span class="input-title">E-mail</span>
      <input type="text" placeholder="Введите ваш E-mail" class="input" />

      <span class="input-title">Телефон</span>
      <input type="text" placeholder="Введите ваше Телефон" class="input" />

      <button class="form-button">Отправить</button>
      <span class="form-agreement"
        >Нажимая кнопку «Отправить», вы даете согласие на обработку персональных
        данных и соглашаетесь с политикой конфиденциальности
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: "FormComponent",
};
</script>

<style lang="scss">

.form-wrapp {
  background: #f2f4f4;
  border-radius: 25px;
  display: flex;
  flex-direction: column;
  padding: 80px;
  margin-top: 150px;
  width: 600px;
  margin: auto;

  .form-title {
    font-size: 30px;
    line-height: 120%;
    color: #4a4a4a;
    text-align: center;
  }

  .input-title {
    font-size: 16px;
    line-height: 12px;
    color: #121621;
    opacity: 0.4;
    margin-bottom: 8px;
  }

  .input {
    background: #ffffff;
    border: 1px solid #dddee4;
    border-radius: 5px;
    margin-bottom: 16px;
    padding: 16px 18px;
  }

  .form-button {
    background: linear-gradient(180deg, #ffa96b -21.43%, #ee7a28 100%);
    border-radius: 10px;
    font-size: 16px;
    line-height: 20px;
    text-align: center;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: #ffffff;
    padding: 14px 15px;
    border: none;
    cursor: pointer;
  }

  .form-agreement {
    font-size: 12px;
    line-height: 16px;
    text-align: center;
    color: #585858;
    margin-top: 16px;
  }
}

@media screen and (max-width: 768px) {
  .form-wrapp {
    padding: 20px;
    width: auto;
    margin: 16px;

    .form-title {
      font-size: 22px;
    }
    
    
  }
}
</style>