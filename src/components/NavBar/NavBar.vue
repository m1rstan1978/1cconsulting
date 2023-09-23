<template>
  <header>
    <div class="header__logo">
        <img class="header__img" src="@/assets/logo/logo.svg">
    </div>
    <div class="header__list" :class="{ 'header__list_active': menuVisible }">
      <ul>
        <li
        v-for="item in listArr"
        :key="item.name"
        @click="clickHere(item.take)"

        >
        {{ item.name }}
        </li>
      </ul>
    </div>
    <div class="header__menu" :class="{ 'header__menu_active': menuVisible }" @click="toggleMenu">
        <div class="header__line"></div>
        <div class="header__line"></div>
        <div class="header__line"></div>
    </div>
  </header>
</template>

<script>
export default {
  data () {
    return {
      menuVisible: false,
      listArr: [
        {
          name: 'клиенты',
          take: '#'
        },
        {
          name: 'контакты',
          take: '#'
        },
        {
          name: 'реквизиты',
          take: '#'
        },
        {
          name: 'договор',
          take: '#'
        },
        {
          name: 'цены',
          take: '#'
        }
      ]
    }
  },
  methods: {
    clickHere (item) {
      const element = document.getElementById(item)
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' })
      }
    },
    toggleMenu () {
      this.menuVisible = !this.menuVisible
    }
  }
}
</script>

<style scoped>
header {
  padding: 30px 20px 30px 20px;
  margin: 0 auto;
  max-width: 1386px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header__img {
  width: 100%;
  height: 100%;
}

.header__logo {
  width: 75px;
  height: 78px;
}
.header__list ul {
  display: flex;
  align-items: center;
}
.header__list ul li {
  font-size: 22px;
  list-style: none;
  margin-left: 77px;
  color: #FFF;
  transition: all 0.3s ease;
  cursor: pointer;
}
.header__list ul li:hover {
  color: #7B52D2;
}

.header__menu {
    width: 30px;
    height: 20px;
    position: absolute;
    top: 40px;
    right: 20px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    cursor: pointer;
    display: none;
}

.header__line {
    width: 100%;
    height: 3px;
    border-radius: 3px;
    background-color: #ffffff;
    transition: transform 0.3s ease;
    margin-bottom: 5px;
}

.header__menu_active .header__line:nth-child(1) {
    transform: translateY(8px) rotate(45deg);
}

.header__menu_active .header__line:nth-child(2) {
    opacity: 0;
}

.header__menu_active .header__line:nth-child(3) {
    transform: translateY(-8px) rotate(-45deg);
}

@media (max-width: 960px) {
  .header__list ul li {
  margin-left: 40px;
}
}

@media (max-width: 760px) {
  .header__list ul li {
    font-size: 18px;
}
  .header__logo {
    width: 55px;
    height: 58px;
}

header {
  padding: 20px 20px 20px 20px;
}
}

@media (max-width: 680px) {
  header {
  flex-direction: column;
  align-items: start;
}

.header__list ul {
  flex-direction: column;
}

.header__list ul li {
  font-size: 20px;
  margin-left: 0px;

}

.header__list {
  margin: 0 auto;
  padding-top: 0px;
  max-height: 0px;
  opacity: 0;
  transition: all .5s ease;
  overflow: hidden;
}

.header__list_active {
  overflow: visible;
  padding-top: 10px;
  max-height: 500px;
  opacity: 1;
}

.header__list ul li:not(:last-child) {
  margin-bottom: 10px;
}

.header__menu {
    display: block;
}
}

</style>
