<script setup lang="ts">
import { getImageUrl } from '@/composables/getImageUrl'

const choices = [
  {
    title: 'Professional o’qituvchilar',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
    img_url: 'choice/img1.png'
  },
  {
    title: 'Tushunarli darslar',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
    img_url: 'choice/img2.png'
  },
  {
    title: 'Ish topishga ko’maklashish',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
    img_url: 'choice/img3.png'
  },
  {
    title: '30% nazariy 70% amaliy',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
    img_url: 'choice/img4.png'
  }
]
</script>

<template>
  <section class="choice">
    <div class="container choice__container">
      <div class="choice__title-wrapper">
        <div class="choice__list-item">
          <div class="choice__list-img-wrapper">
            <img class="choice__list-img" src="@/assets/images/choice/img5.png" alt="icon" />
          </div>
          <div class="choice__list-inner">
            <h3 class="choice__list-title">Yuqori natija</h3>
            <p class="choice__list-text">
              Lorem Ipsum is simply dummy text of the printing and typesetting industry.
            </p>
          </div>
        </div>
        <h2 class="choice__title base-title">
          Nima uchun mijozlar bizni <span class="base-title-red">kursni tanlab kelishadi ?</span>
        </h2>
      </div>
      <ul class="choice__list">
        <li v-for="choice in choices" :key="choice.img_url" class="choice__list-item">
          <div class="choice__list-img-wrapper">
            <img class="choice__list-img" :src="getImageUrl(choice.img_url)" alt="img" />
          </div>
          <div class="choice__list-inner">
            <h3 class="choice__list-title">{{ choice.title }}</h3>
            <p class="choice__list-text">{{ choice.text }}</p>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>
