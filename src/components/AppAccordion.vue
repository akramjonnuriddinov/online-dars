<script setup lang="ts">
import TheTransition from '@/components/TheTransition.vue'
import { ref } from 'vue'

defineProps(['expanded'])

const contents = ref([
  {
    isOpen: false,
    number: '1- Modul',
    title: 'Kirish va boshlang’ich bilimlar',
    text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, <strong> when an unknown printer took a galley of type and scrambled it to make </strong>",
    lessons: [
      {
        lesson_number: '1- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      },
      {
        lesson_number: '2- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      },
      {
        lesson_number: '3- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      },
      {
        lesson_number: '4- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      }
    ]
  },
  {
    isOpen: false,
    number: '2- Modul',
    title: 'Kirish va boshlang’ich bilimlar',
    text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, <strong> when an unknown printer took a galley of type and scrambled it to make </strong>",
    lessons: [
      {
        lesson_number: '5- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      },
      {
        lesson_number: '6- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      },
      {
        lesson_number: '7- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      },
      {
        lesson_number: '8- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      }
    ]
  },
  {
    isOpen: false,
    number: '3- Modul',
    title: 'Kirish va boshlang’ich bilimlar',
    text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, <strong> when an unknown printer took a galley of type and scrambled it to make </strong>",
    lessons: [
      {
        lesson_number: '9- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      },
      {
        lesson_number: '10- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      },
      {
        lesson_number: '11- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      },
      {
        lesson_number: '12- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      }
    ]
  },
  {
    isOpen: false,
    number: '4- Modul',
    title: 'Kirish va boshlang’ich bilimlar',
    text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, <strong> when an unknown printer took a galley of type and scrambled it to make </strong>",
    lessons: [
      {
        lesson_number: '23- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      },
      {
        lesson_number: '24- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      },
      {
        lesson_number: '25- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      },
      {
        lesson_number: '26- dars',
        theme: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.'
      }
    ]
  }
])
</script>

<template>
  <ul class="accordion-list">
    <li
      v-for="content in contents"
      :key="content.number"
      @click="content.isOpen = !content.isOpen"
      class="accordion-list__item"
    >
      <div class="accordion-list__header">
        <img
          class="accordion-list__icon"
          :class="{ 'accordion-list__icon--open': expanded }"
          src="/src/assets/images/accordion-icon.svg"
          alt="accordion_icon"
        />
        <span class="accordion-list__header-number">{{ content.number }}</span>
        <h3 class="accordion-list__header-title">{{ content.title }}</h3>
      </div>
      <the-transition>
        <div v-if="content.isOpen" class="accordion-list__inner">
          <p v-html="content.text" class="accordion-list__inner-text"></p>
          <ul class="lesson-list">
            <li
              v-for="lesson in content.lessons"
              :key="lesson.lesson_number"
              class="lesson-list__item"
            >
              <span class="lesson-list__number">{{ lesson.lesson_number }}</span>
              <p class="lesson-list__theme">{{ lesson.theme }}</p>
            </li>
          </ul>
        </div>
      </the-transition>
    </li>
  </ul>
</template>

<style scoped></style>
