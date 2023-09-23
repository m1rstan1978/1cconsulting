<template>
  <div class="about">
    <h1 class="about__title">1С Профессиональное Сопровождение</h1>
    <div class="about__menu">
        <p class="about__1c">Консалтинг по 1С</p>
    </div>
    <div class="about__content">
        <div
        class="about__item"
        v-for="item in arrList"
        :key="item.id"
      >
        <p class="about__text">{{ item }}</p>
      </div>
    </div>
    <div class="about__block">
        <div class="about__item1">
        <p class="about__text">Сопровождение и удалённая поддержка</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      arrList: [
        'Установка и внедрение 1С предприятие',
        'Обучение возможностям типовых конфигураций',
        'Подготовка технического задания',
        'Конфигурирование индивидуальных настроек',
        'Настройка обмена с сайтами, СRM, Маркетплэйсами',
        'Настройка обмена данными'
      ]
    }
  }
}
</script>

<style scoped>
.about {
    padding-bottom: 100px;
}
.about__title{
    text-align: center;
    color: #FFF;
    font-size: 48px;
    padding-bottom: 40px;
    font-weight: 700;
    max-width: 581px;
    margin: 0 auto;
}
.about__menu{
    display: flex;
    align-items: center;
    justify-content: center;

}
.about__1c {
    color: #FFF;
    font-size: 26px;
    font-weight: 400;
    padding: 30px 80px;
    border-radius: 45px;
    border: 3px solid #7B51D2;
    background: #7B51D2;
    margin-bottom: 60px;
}
.about__content {
    display: grid;
    grid-template-columns:repeat(3, 1fr);
    grid-column-gap: 40px;
    grid-row-gap: 40px;
    justify-items: center;
    margin: 0 auto;
    max-width: 1320px;
    padding: 0 20px;
    padding-bottom: 40px;
}
.about__item {
    padding: 20px 62px;
    border-radius: 45px;
    border: 2px solid #7B51D2;
    display: flex;
    align-items: center;
    justify-content: center;
}
.about__item1 {
    padding: 20px 32px;
    border-radius: 45px;
    border: 2px solid #7B51D2;
    display: flex;
    align-items: center;
    justify-content: center;
}

.about__text {
    text-align: center;
    color: #FFF;
    font-size: 20px;
    font-weight: 400;
    max-width: 340px;
}
.about__block {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 0 20px;
}

@media (max-width: 1200px) {
    .about__content {
        grid-template-columns:repeat(2, 1fr);
    grid-column-gap: 40px;
    grid-row-gap: 40px;
    max-width: 850px;
}
.about {
    padding-bottom: 80px;
}
}

@media (max-width: 900px) {
    .about__content {
        grid-template-columns:repeat(1, 1fr);
    grid-column-gap: 40px;
    grid-row-gap: 40px;
    max-width: 450px;
}

.about {
    padding-bottom: 60px;
}
}

@media (max-width: 750px) {
    .about__title {
        font-size: 38px;
    }

    .about__1c {
        font-size: 20px;
        margin-bottom: 50px;
    }

    .about__item {
        padding: 15px 40px;
    }

    .about__item1 {
        padding: 15px 40px;
    }
}

@media (max-width: 500px) {
    .about__title {
        font-size: 28px;
        padding-bottom: 35px;
    }

    .about__1c {
        padding: 20px 60px;
        margin-bottom: 40px;
    }

    .about__text {
        font-size: 18px;
        max-width: 340px;
    }

    .about__content {
    grid-row-gap: 30px;
    padding-bottom: 30px;
}

.about {
    padding-bottom: 40px;
}
}
</style>
