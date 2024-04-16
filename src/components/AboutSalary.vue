<script setup lang="ts">
import { getImageUrl } from '@/composables/getImageUrl'

const images = [
  {
    img_url: 'salary/salary-1.jpg',
    link: '#'
  },
  {
    img_url: 'salary/salary-1.jpg',
    link: '#'
  },
  {
    img_url: 'salary/salary-1.jpg',
    link: '#'
  },
  {
    img_url: 'salary/salary-1.jpg',
    link: '#'
  }
]
</script>

<template>
  <section class="about-salary">
    <div class="container about-salary__container">
      <div class="about-salary__header">
        <div class="about-salary__header-content">
          <h2 class="about-salary__title base-title">
            UX/UI DESIGNERLARNI XOZIRDA <span class="base-title-red">OYLIKLARI QANCHA?</span>
          </h2>
          <p class="about-salary__text">
            Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum
            has
          </p>
        </div>
        <img src="/src/assets/images/salary/salary-hero.png" alt="icon" />
      </div>
      <div class="about-salary__footer">
        <ul class="about-salary__list">
          <li v-for="image in images" :key="image.link" class="about-salary__item">
            <img class="about-salary__item-img" :src="getImageUrl(image.img_url)" alt="img" />
            <a class="about-salary__item-link" :href="image.link" target="_blank"
              >Olingan manba orqali ko’rish</a
            >
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
