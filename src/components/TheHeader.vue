<script setup lang="ts">
import TheLogo from '@/components/TheLogo.vue'
import BaseButton from '@/components/BaseButton.vue'

const links = [
  {
    name: 'Muallifdan video',
    path: 'owner_videos'
  },
  {
    name: 'Muallif haqida',
    path: 'about_owner'
  },
  {
    name: 'Kurs qanday tashkil topgan',
    path: 'about_course'
  },
  {
    name: 'Izohlar',
    path: 'comments'
  }
]
</script>

<template>
  <header class="header">
    <div class="container header__container">
      <router-link to="/">
        <the-logo />
      </router-link>
      <ul class="header__list">
        <li v-for="link in links" :key="link.path" class="header__list-item">
          <router-link :to="link.path" class="header__list-link">{{ link.name }}</router-link>
        </li>
      </ul>
      <base-button />
    </div>
  </header>
</template>
