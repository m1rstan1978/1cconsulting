<template>
  <div class="banner">
    <NavBar></NavBar>
    <div class="banner__block">
    <VueTyped
    :strings="typedStrings"
    :typeSpeed="40"
    :backSpeed="20"
    :loop="true"
    class="banner__text"
    ></VueTyped>
    </div>
    <div class="banner__content">
      <div class="banner__el1">
        <img src="@/assets/circles/1.svg">
    </div>
    <div class="banner__el2">
        <img src="@/assets/circles/2.svg">
    </div>
    <div class="banner__el3">
        <img src="@/assets/circles/3.svg">
    </div>
    <div class="banner__el4">
        <img src="@/assets/circles/4.svg">
    </div>
    <div class="banner__arrow">
        <div class="banner__image">
            <img src="@/assets/circles/5.svg">
        </div>
    </div>
    </div>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar/NavBar.vue'

export default {
  data () {
    return {
      typedStrings: [
        'Оперативное внедрение и настройка 1С',
        '1С: Быстро и точно!',
        '1С: Точность – залог успеха!']
    }
  },
  components: { NavBar }
}
</script>

<style scoped>
.banner {
    position: relative;
    height: 100vh;
}
.banner__block {
    position: relative;
    height: 250px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 15.4444vh;
    z-index: 2;
}
.banner__text {
    text-align: center;
    color: #FFF;
    font-size: 74px;
    font-weight: 800;
    max-width: 980px;
}
.banner__des {
    text-align: center;
    color: #7B51D2;
    font-size: 18px;
    font-weight: 600;
}
.banner__el1 {
    position: absolute;
    top: 15%;
    left: 35%;
    animation: moveRandomly 10s linear infinite;
}
.banner__el2 {
    position: absolute;
    top: 10%;
    left: 80%;
    animation: swim 7s linear infinite;
}
.banner__el3 {
    position: absolute;
    top: 50%;
    left: 15%;
    animation: float 7s linear infinite;
}
.banner__el4 {
    position: absolute;
    top: 60%;
    left: 75%;
    animation: moveInCircle 7s linear infinite;
}
.banner__arrow {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 23.4444vh;
    animation: ring 1s infinite ease-in-out;
    transition: all 0.3s ease;
    cursor: pointer;
}

@keyframes moveRandomly {
    0% {
      transform: translate(-50%, -50%) translateX(0px) translateY(0px);
    }
    25% {
      transform: translate(-50%, -50%) translateX(50px) translateY(50px);
    }
    50% {
      transform: translate(-50%, -50%) translateX(-30px) translateY(-70px);
    }
    75% {
      transform: translate(-50%, -50%) translateX(70px) translateY(-30px);
    }
    100% {
      transform: translate(-50%, -50%) translateX(0px) translateY(0px);
    }
  }
  @keyframes swim {
    0% {
        transform: translate(0, 0);
    }
    25% {
        transform: translate(30px, 30px);
    }
    50% {
        transform: translate(0, 0);
    }
    75% {
        transform: translate(-30px, -30px);
    }
}
@keyframes float {
    0% {
        transform: translateY(0);
    }
    50% {
        transform: translateY(40px);
    }
    100% {
        transform: translateY(0);
    }
}
@keyframes moveInCircle {
    0% {
        transform: translateX(0%) translateY(-30%);
      }
      25% {
        transform: translateX(30%) translateY(0%);
      }
      50% {
        transform: translateX(0%) translateY(30%);
      }
      75% {
        transform: translateX(-30%) translateY(0%);
      }
      100% {
        transform: translateX(0%) translateY(-30%);
      }
  }
  @keyframes ring {
    0% {
    transform: translateY(0);
  }
  25% {
    transform: translateY(-12px);
  }
  50% {
    transform: translateY(0);
  }
  75% {
    transform: translateY(-5px);
  }
  100% {
    transform: translateY(0) ;
  }
}

@media (max-width:1200px) {
  .banner__text {
    font-size: 64px;
  }

  .banner__el2 {
    display: none;
  }
}

@media (max-width:900px) {
  .banner__text {
    font-size: 44px;
    max-width: 600px;
    padding: 0 20px;
  }
}

@media (max-width:450px) {

  .banner__el4 {
    display: none;
  }
}
</style>
