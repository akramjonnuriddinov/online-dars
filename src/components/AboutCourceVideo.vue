<script setup lang="ts"></script>

<template>
  <section class="about-video">
    <div class="container about-video__container">
      <h2 class="about-video__title base-title">
        muallifdan <span class="base-title-red">kurs haqida video</span>
      </h2>
      <p class="about-video__text">
        Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum
      </p>
      <div class="video">
        <img class="video__img" src="@/assets/images/video/video-top.jpg" alt="course" />
        <iframe
          class="video__embed"
          width="695"
          height="391"
          src="https://www.youtube.com/embed/eVV_XZPQ7bc"
          title="Hamma narsani 100% samarali o&#39;rganing!"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin"
          allowfullscreen
        ></iframe>
      </div>
    </div>
  </section>
</template>
