<script setup lang="ts">
const contents = [
  {
    id: '1',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting '
  },
  {
    id: '2',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting '
  },
  {
    id: '3',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting '
  },
  {
    id: '4',
    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting '
  }
]
</script>

<template>
  <section class="creator">
    <div class="container creator__container">
      <img class="creator__img" src="@/assets/images/creator/creator.png" alt="creator" />
      <div class="creator__inner">
        <span class="creator__subtitle">Kurs muallifi</span>
        <h2 class="base-title creator__title">Eshonov Fakhriyor</h2>
        <p class="creator__text">
          Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has
          been the industry's
        </p>
        <ul class="creator__inner-list">
          <li v-for="content in contents" :key="content.id" class="creator__inner-list-item">
            <div class="creator__inner-list-img-wrapper">
              <img
                class="creator__inner-list-img"
                src="/src/assets/images/creator/check.svg"
                alt="check_icon"
              />
            </div>
            <p class="creator__inner-list-text">{{ content.text }}</p>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
