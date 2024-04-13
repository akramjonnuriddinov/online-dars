<script setup lang="ts">
import { getImageUrl } from '@/composables/getImageUrl'

const contents = [
  {
    title: 'IT - sohasidagi yangi mehmonlarga',
    text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged",
    img_url: 'course/img1.png'
  },
  {
    title: 'IT - sohasida mutaxassistlar bilmlarini oshirishi uchun',
    text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged",
    img_url: 'course/img2.png'
  },
  {
    title: 'O’z hayotini tubdan o’zgartirmoqchilar uchun',
    text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged",
    img_url: 'course/img3.png'
  }
]
</script>

<template>
  <section class="course">
    <div class="container course__container">
      <h2 class="course__title base-title">
        Kurslarimiz kimlarga <span class="base-title-red">Tavsiya qilinadi?</span>
      </h2>
      <ul class="course__list">
        <li v-for="content in contents" :key="content.img_url" class="course__list-item">
          <div class="course__list-img-wrapper">
            <img class="course__list-img" :src="getImageUrl(content.img_url)" alt="icon" />
          </div>
          <div class="course__list-inner">
            <h3 class="course__list-inner-title">{{ content.title }}</h3>
            <p class="course__list-inner-text">{{ content.text }}</p>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>
