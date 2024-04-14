<script setup lang="ts">
import { getImageUrl } from '@/composables/getImageUrl'

const benifits = [
  {
    text: 'Istalgan joyda ishlay olish',
    img_url: 'hero/img1.png',
    bg_color: '#FFE5E5',
    max_width: '239px'
  },
  {
    text: 'O’zi - o’ziga ho’jayin bo’la olish',
    img_url: 'hero/img2.png',
    bg_color: '#E8F4FF',
    max_width: '261px'
  },
  {
    text: 'Yaxshi maosh qozonish',
    img_url: 'hero/img3.png',
    bg_color: '#E5FFE9',
    max_width: '239px'
  },
  {
    text: 'Va albatta katta muvaffaqiyatlarga erishish',
    img_url: 'hero/img4.png',
    bg_color: '#F0FAFF',
    max_width: '271px'
  }
]
</script>

<template>
  <section class="hero">
    <div class="container hero__container">
      <div class="hero__inner">
        <span class="hero__inner-text">Umr o’tib ketmoqda....</span>
        <h1 class="hero__title base-title">
          Balkim <span class="base-title-red hero__title--red">zamonaviy</span> kasbni o’rganish
          vaqti kelgandir?
        </h1>
        <p class="hero__text">Zamonaviy kasb o’rganishni afzalliklari</p>
        <ul class="hero__list">
          <li
            v-for="benifit in benifits"
            :key="benifit.img_url"
            :style="{ 'max-width': benifit.max_width }"
            class="hero__list-item"
          >
            <div :style="{ backgroundColor: benifit.bg_color }" class="hero__list-img-wrapper">
              <img class="hero__list-img" :src="getImageUrl(benifit.img_url)" alt="img" />
            </div>
            <span class="hero__list-text">{{ benifit.text }}</span>
          </li>
        </ul>
      </div>
    </div>
    <div class="hero__img-bg">
      <div class="hero__img-wrapper">
        <img class="hero__img" src="@/assets/images/hero/hero-img2.png" alt="" />
      </div>
    </div>
  </section>
</template>
