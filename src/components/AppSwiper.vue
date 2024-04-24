<script setup lang="ts">
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import { getImageUrl } from '@/composables/getImageUrl'

const onSwiper = () => {}
const onSlideChange = () => {}

const users = [
  {
    name: 'Eshonov fakhriyor',
    user_info:
      "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.  It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s",
    img_url: 'swiper/user.jpg'
  },
  {
    name: 'Eshonov fakhriyor',
    user_info:
      "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.  It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s",
    img_url: 'swiper/user.jpg'
  },
  {
    name: 'Eshonov fakhriyor',
    user_info:
      "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.  It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s",
    img_url: 'swiper/user.jpg'
  },
  {
    name: 'Eshonov fakhriyor',
    user_info:
      "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.  It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s",
    img_url: 'swiper/user.jpg'
  }
]
</script>

<template>
  <section id="comments" class="app-swiper">
    <div class="container app-swiper__container">
      <div class="app-swiper__header">
        <h2 class="app-swiper__title base-title">
          Kurs haqida <span class="base-title-red">izohlar </span>
        </h2>
        <div class="app-swiper__btn-wrapper">
          <button class="app-swiper__header-dark-btn swiper-btn">
            <img src="/src/assets/images/swiper/right.svg" alt="right_icon" />
          </button>
          <button class="app-swiper__header-red-btn swiper-btn">
            <img src="/src/assets/images/swiper/left.svg" alt="left_icon" />
          </button>
        </div>
      </div>
    </div>
    <!-- SWIPER -->
    <swiper
      class="swiper"
      :slides-per-view="2"
      :space-between="0"
      @swiper="onSwiper"
      @slideChange="onSlideChange"
    >
      <swiper-slide v-for="user in users" :key="user.name" class="swiper-slide">
        <div class="swiper-slide-custom">
          <img
            class="swiper-slide__img"
            width="305"
            height="305"
            :src="getImageUrl(user.img_url)"
            alt="user"
          />
          <div class="swiper-slide__inner">
            <h3 class="swiper-slide__title">{{ user.name }}</h3>
            <p class="swiper-slide__text">
              {{ user.user_info }}
            </p>
          </div>
        </div>
      </swiper-slide>
    </swiper>
    <!-- /SWIPER -->
    <div class="app-swiper__btn-wrapper swiper-bottom">
      <button class="app-swiper__header-dark-btn swiper-btn">
        <img src="/src/assets/images/swiper/right.svg" alt="right_icon" />
      </button>
      <button class="app-swiper__header-red-btn swiper-btn">
        <img src="/src/assets/images/swiper/left.svg" alt="left_icon" />
      </button>
    </div>
  </section>
</template>

<style scoped></style>
