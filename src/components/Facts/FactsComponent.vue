<template>
  <div class="facts">
    <h1 class="facts__title">О нас в цифрах </h1>
    <div class="facts__content">
        <div class="facts__image">
            <img class="facts__img" src="@/assets/facts/facts.svg">
        </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.facts {
    padding-bottom: 100px;
}
.facts__title {
    text-align: center;
    color: #FFF;
    font-size: 48px;
    padding-bottom: 40px;
    font-weight: 700;
}
.facts__content {
    display: flex;
    align-items: center;
    justify-content: center;
}

.facts__image {
    padding: 0 20px;
}

@media (max-width: 1200px) {
    .facts {
    padding-bottom: 80px;
}
}

@media (max-width: 900px) {
    .facts__img {
        max-width: 100%;
        height: auto;
    }

    .facts {
    padding-bottom: 60px;
}
}

@media (max-width: 750px) {
    .facts__title {
    font-size: 38px;
}
}

@media (max-width: 500px) {
    .facts__title {
    padding-bottom: 30px;
}
.facts__title {
    font-size: 28px;
}

.facts {
    padding-bottom: 40px;
}
}
</style>
