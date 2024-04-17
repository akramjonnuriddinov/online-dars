<script setup lang="ts">
import { ref } from 'vue'
import { updateNumber } from '@/composables/usePhone'

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
  }
]

const phone = ref()
</script>

<template>
  <section class="contact">
    <div class="container contact__container">
      <div class="contact__base contact__info">
        <h3 class="contact__base-title">KURS NARXI</h3>
        <span class="contact__price">500 000 SO’M / OY</span>
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
      <form class="contact__base contact__form" action="POST">
        <h3 class="contact__base-title">TEZKOR SOTIB OLISH</h3>
        <label class="contact__form-field" for="name">
          <span class="contact__form-text">ISM</span>
          <input
            class="contact__form-input"
            id="name"
            type="text"
            placeholder="(Fakhriyor)"
            autocomplete="off"
          />
        </label>
        <label class="contact__form-field" for="phone">
          <span class="contact__form-text">TELEFON RAQAMINGIZ</span>
          <input
            v-model="phone"
            class="contact__form-input"
            id="phone"
            type="tel"
            placeholder="+998 (--) --- -- --"
            @input="phone = updateNumber(phone)"
            autocomplete="off"
          />
        </label>
      </form>
    </div>
  </section>
</template>
