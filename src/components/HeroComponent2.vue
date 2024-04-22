<script setup lang="ts">
import { getImageUrl } from '@/composables/getImageUrl'

const benifits = [
  {
    text: 'Istalgan joyda ishlay olish',
    img_url: 'hero/site-hero/img1.svg',
    bg_color: '#FFE5E5',
    max_width: '239px'
  },
  {
    text: 'O’zi - o’ziga ho’jayin bo’la olish',
    img_url: 'hero/site-hero/img2.svg',
    bg_color: '#E8F4FF',
    max_width: '261px'
  },
  {
    text: 'Yaxshi maosh qozonish',
    img_url: 'hero/site-hero/img3.svg',
    bg_color: '#E5FFE9',
    max_width: '239px'
  },
  {
    text: 'Va albatta katta muvaffaqiyatlarga erishish',
    img_url: 'hero/site-hero/img4.svg',
    bg_color: '#F0FAFF',
    max_width: '271px'
  }
]
</script>

<template>
  <section class="site-hero">
    <div class="container site-hero__container">
      <img
        class="site-hero__img"
        src="@/assets/images/hero/hero2-img.svg"
        alt="hero illustriation"
      />
      <div class="site-hero__inner">
        <div class="site-hero__inner-top">
          <span class="site-hero__inner-text">Umr o’tib ketmoqda....</span>
          <h1 class="base-title site-hero__title">
            Balkim <span class="base-title-red">zamonaviy</span> kasbni o’rganish vaqti kelgandir?
          </h1>
        </div>
        <div class="site-hero__list-wrapper">
          <p class="site-hero__list-text">Zamonaviy kasb o’rganishni afzalliklari</p>
          <ul class="site-hero__list">
            <li v-for="benifit in benifits" :key="benifit.img_url" class="site-hero__item">
              <img :src="getImageUrl(benifit.img_url)" alt="hero" class="site-hero__item-img" />
              <p class="site-hero__item-text">{{ benifit.text }}</p>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.site-hero {
  background-image: url('@/assets/images/hero/hero2-bg.svg');
  background-repeat: no-repeat;
  background-size: contain;
  margin-bottom: 80px;
}

.site-hero__container {
  display: flex;
  flex-direction: column;
  row-gap: 90px;
}

.site-hero__list {
  display: flex;
  flex-wrap: wrap;
  row-gap: 38px;
  column-gap: 26px;
}

.site-hero__item {
  max-width: 178px;
  width: 100%;
  display: flex;
  flex-direction: column;
  text-align: center;
  align-items: center;
}
.site-hero__item:nth-child(2n + 1) {
  max-width: 128px;
}

.site-hero__item-img {
  width: 73px;
  height: 73px;
}

.site-hero__title {
  margin-bottom: 30px;
  text-align: center;
}

.site-hero__inner-text {
  color: black;
  margin-bottom: 24px;
  text-transform: uppercase;
  font-size: 16px;
  line-height: 21.82px;
  display: block;
  text-align: center;
}

.site-hero__list-text {
  margin-top: 0;
  margin-bottom: 30px;
  font-weight: 700;
  font-size: 24px;
  line-height: 32.74px;
  color: black;
  text-align: center;
}

.site-hero__item-text {
  margin: 0;
  font-size: 20px;
  line-height: 27.28px;
}

@media screen and (min-width: 768px) {
  .site-hero__title {
    font-size: 40px;
    line-height: 50px;
    text-align: left;
    margin-bottom: 59px;
  }
  .site-hero__inner-text {
    text-align: left;
  }
  .site-hero__list-text {
    text-align: left;
  }
  .site-hero__list {
    row-gap: 36px;
    column-gap: 58px;
  }
  .site-hero__item {
    flex-direction: row;
    align-items: center;
    text-align: left;
    max-width: 271px;
  }
  .site-hero__item:nth-child(2n + 1) {
    max-width: 239px;
  }
  .site-hero__item-img {
    margin-right: 20px;
    margin-bottom: 0;
  }
}

@media screen and (min-width: 1200px) {
  .site-hero {
    background-position: left calc(50% + 526px) top;
    padding-top: 20px;
    padding-bottom: 73px;
  }
  .site-hero__container {
    flex-direction: row-reverse;
    justify-content: flex-end;
  }
  .site-hero__img {
    width: 100%;
  }
  .site-hero__inner {
    max-width: 622px;
    width: 100%;
    margin-right: 30px;
  }
}
</style>
