<template>
  <footer>
    <div class="footer__image">
        <img class="footer__img" src="@/assets/logo/logo.svg">
    </div>
    <div class="footer__content">
        <div class="footer__logo">
            <p class="footer__text">ИП Коваль Станислав Сергеевич </p>
            <p class="footer__text">ИНН 434540685476</p>
        </div>
        <p class="footer__text footer__text_special">Все права защищены</p>
        <div class="footer__info">
            <p class="footer__text">г.Лагань, ул Куйбышева, 77</p>
            <p class="footer__text">+7 (922)940-45-45</p>
            <p class="footer__text">Koval.st@mail.ru</p>
        </div>
    </div>
  </footer>
</template>

<script>
export default {

}
</script>

<style scoped>
footer {
  position: relative;
  margin: 0 auto;
  max-width: 1386px;
  padding: 0 20px 40px 20px;
}
.footer__content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: none;
}
.footer__text {
    color: #B9B7B7;
    font-size: 14px;
    font-weight: 300;
}

.footer__img {
  width: 100%;
  height: 100%;
}

.footer__image {
  width: 75px;
  height: 78px;
}
@media (max-width: 760px) {
.footer__image {
  width: 55px;
  height: 58px;
}
}

@media (max-width: 700px) {
  .footer__image {
    margin: 0 auto;
  }

  .footer__content {
    flex-direction: column;
  }

  .footer__text {
    text-align: center;
    margin-top: 5px;
}

.footer__text_special {
  color: #7B51D2;
}
}
</style>
