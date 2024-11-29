<script setup>
import { ref, onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css';


import navOpenIcon from '@/assets/img/icons/nav-open.svg';
import navCloseIcon from '@/assets/img/icons/nav-close.svg';

const navOpen = ref(false);
const navBtnImg = ref(navOpenIcon);

const toggleNav = () => {
  navOpen.value = !navOpen.value;
  navBtnImg.value = navOpen.value ? navOpenIcon : navCloseIcon;
};

onMounted(() => {
  AOS.init();
});
</script>

<template>
  <header class="header">
    <div class="container">
      <div class="header-nav">
        <a href="#!" class="logo">Kelvin</a>
        <nav :class="{ nav: true, open: navOpen }">
          <ul class="nav-list">
            <li class="nav-item"><a href="#!" class="nav-link active">Home</a></li>
            <li class="nav-item"><a href="#!" class="nav-link">Works</a></li>
            <li class="nav-item"><a href="#!" class="nav-link">Services</a></li>
            <li class="nav-item"><a href="#!" class="nav-link">About</a></li>
            <li class="nav-item"><a href="#!" class="nav-link">Contact</a></li>
          </ul>
          <button class="nav-button" @click="toggleNav">
            <img :src="navBtnImg" alt="X">
          </button>
        </nav>
      </div>
      <div class="header-row">
        <div class="header-content" data-aos="fade-up">
          <h1 class="header-heading">Kelvin Kramer<br> <span>Designer & Developer</span></h1>
          <p>I’m a portrait, fashion and lifestyle photographer living In New York City. During my thirteen year tenure here.</p>
        </div>
        <div class="header-img" data-aos="fade-left">
          <picture>
            <source media="(max-width: 799px)" srcset="@/assets/img/header/hero-mobile.png">
            <img src="@/assets/img/header/hero.png" alt="">
          </picture>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped>
.header {
  padding-top: 46px;
  background-color: #F1F1F1;
}

.header-nav {
  display: flex;
  justify-content: space-between;
  align-items: flex-end;

  margin-bottom: 76px;
}

.logo {
  position: relative;
  padding: 0 12px 3px 0;

  font-weight: 700;
  font-size: 32px;
  line-height: 1;
  color: #000;
}

.logo::after {
  position: absolute;
  right: 0;
  bottom: 0;

  content: "";
  display: block;
  width: 8px;
  height: 8px;
  background-color: #FDA300;
  border-radius: 50%;
}


.nav-list {
  display: flex;
  column-gap: 50px;
  font-weight: 500;
  font-size: 14px;
}

.nav-button {
  display: none;
}

.nav-link {
  color: #000;
}

.nav-link.active {
  color: #606060;
}

.header-row {
  display: flex;justify-content: space-between;
  column-gap: 30px;
}

.header-content {
  margin-top: 124px;
  max-width: 500px;
}

.header-heading {
  margin-bottom: 20px;
  font-weight: 600;
  font-size: 44px;
}

.header-content p {
  line-height: 2;
}
@media (max-width: 1230px) {
  .nav-list {
    display: none;
  }

  .nav-button {
    display: block;
  }

  .nav.open .nav-list {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: #fff;

    z-index: 1;
    padding: 46px 30px;
    display: flex;
    flex-direction: column;
    row-gap: 40px;

    font-size: 34px;
    font-weight: 600;
  }

  .nav-link {
    color: #828282;
  }

  .nav-link.active {
    color: #000;
  }

  .nav-button {
    position: absolute;
    z-index: 9;
    top: 46px;
    right: 30px;
  }

  .nav.open .nav-button {
    position: fixed;
  }

  .header-nav {
    margin-bottom: 50px;
  }

  .header-row {
    flex-direction: column;
    row-gap: 20px;
  }

  .header-content {
    margin-top: 0;
  }

  .header-img {
    text-align: center;
  }
}
@media (max-width: 700px) {
  .header-heading {
    font-size: 34px;
    line-height: 1.3;
  }

  .header-heading span {
    font-size: 28px;
  }

}
</style>