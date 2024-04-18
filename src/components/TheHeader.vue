<script setup lang="ts">
import TheLogo from '@/components/TheLogo.vue'
import BaseButton from '@/components/BaseButton.vue'
import { ref, onUpdated } from 'vue'

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
const isOpen = ref(false)

const toggleMenu = () => {
  isOpen.value = !isOpen.value
}

onUpdated(() => {
  if (isOpen.value) {
    document.body.classList.add('overflow-hidden')
  }
})
</script>

<template>
  <header class="header">
    <div class="container header__container">
      <router-link class="header__logo" to="/">
        <the-logo />
      </router-link>
      <nav class="header__nav" :class="{ 'header__nav--open': isOpen }">
        <button @click="toggleMenu" class="open-menu close-menu">
          <img src="@/assets/images/close.svg" alt="" />
        </button>
        <ul class="header__list">
          <li v-for="link in links" :key="link.path" class="header__list-item">
            <router-link :to="link.path" class="header__list-link">{{ link.name }}</router-link>
          </li>
        </ul>
        <base-button class="header__tablet-btn" />
      </nav>
      <base-button />
      <button @click="toggleMenu" class="open-menu">
        <img src="@/assets/images/menu.svg" alt="" />
      </button>
    </div>
    <div
      @click="toggleMenu"
      class="header__transparent-bg"
      :class="{ 'header__transparent-bg--open': isOpen }"
    ></div>
  </header>
</template>

<style scoped>
.header__transparent-bg {
  position: fixed;
  background-color: #00000080;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 9;
  display: none;
}

.header__transparent-bg--open {
  display: flex;
}
</style>
