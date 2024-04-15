<script setup lang="ts">
const counts = [
  {
    number: 50,
    text: 'Darslar'
  },
  {
    number: 81,
    text: 'Lorem Ipsum is simply dummy'
  },
  {
    number: 187,
    text: 'Lorem Ipsum is simply dummy'
  },
  {
    number: 1008,
    text: 'Lorem Ipsum is simply dummy'
  }
]
</script>

<template>
  <section class="course-count">
    <div class="container course-count__container">
      <h2 class="course-count__title base-title">
        Kurs xarakteristikasi <span class="base-title-red">sonlarda</span>
      </h2>
      <ul class="course-count__list">
        <li v-for="count in counts" :key="count.number" class="course-count__list-item">
          <span class="course-count__list-number">{{ count.number }}</span>
          <p class="course-count__list-text">{{ count.text }}</p>
        </li>
      </ul>
    </div>
  </section>
</template>

<style scoped></style>
