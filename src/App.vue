<template>
  <div class="main">
    <div class="main__content">
      <MainBannerComponent></MainBannerComponent>
      <AboutComponent></AboutComponent>
      <FactsComponent></FactsComponent>
      <footer-vue></footer-vue>
    </div>
  </div>
</template>

<script>
import MainBannerComponent from './components/MainBanner/MainBannerComponent.vue'
import AboutComponent from './components/About/AboutComponent.vue'
import FactsComponent from './components/Facts/FactsComponent.vue'
import FooterVue from './components/Footer/FooterVue'

export default {
  components: { MainBannerComponent, AboutComponent, FactsComponent, FooterVue }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@300;400;500;600;700;800;900;1000&display=swap');
* {
  font-family: 'Nunito', sans-serif;
  margin: 0;
  padding: 0;

}
.main {
  background: linear-gradient(180deg, #1A2053 0%, #040617 100%);
}
.main__content {
  width: 100%;
  margin: 0 auto;
  max-width: 1920px;
}
</style>
