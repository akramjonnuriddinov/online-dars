<script setup lang="ts">
import LogoDark from '@/components/LogoDark.vue'
</script>

<template>
  <footer class="footer">
    <div class="container footer__container">
      <div class="footer__info">
        <router-link to="/" class="footer__logo">
          <logo-dark />
        </router-link>
        <p class="footer__text">
          Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has
          been the industry's standard dummy text ever since the 1500s,
        </p>
        <span class="footer__privacy">Barcha huquqlar himoyalangan</span>
      </div>
      <div class="footer__contact">
        <span class="footer__contact-text">Qo’shimcha ma’lumot uchun</span>
        <div class="footer__contact-phone-wrapper">
          <img class="footer__contact-phone" src="@/assets/images/phone.svg" alt="phone" />
          <span>+998 97 628 28 82</span>
        </div>
      </div>
    </div>
  </footer>
</template>
