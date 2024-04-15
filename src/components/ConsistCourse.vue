<script setup lang="ts">
import AppAccordion from '@/components/AppAccordion.vue'

const consists = [
  {
    number: '36+',
    text: 'Uyga vazifalar'
  },
  {
    number: '5+',
    text: 'Portfolioga real ishlar'
  }
]
</script>

<template>
  <section class="consist-course">
    <div class="container consist-course__container">
      <div class="consist-course__inner">
        <h2 class="consist-course__title base-title">
          Kurs qanday <span class="base-title-red">Tashkil topgan? </span> ?
        </h2>
        <div class="consist-course__content">
          <p class="consist-course__text">
            Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum
            has been the industry's standard dummy text ever since the 1500s, when an unknown
            printer took a galley of type
          </p>
          <ul class="consist-course__list">
            <li v-for="consist in consists" :key="consist.number" class="consist-course__list-item">
              <span class="consist-course__list-number">{{ consist.number }}</span>
              <p class="consist-course__list-text">{{ consist.text }}</p>
            </li>
          </ul>
        </div>
      </div>
      <app-accordion />
    </div>
  </section>
</template>
