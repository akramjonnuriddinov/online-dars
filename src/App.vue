<script setup lang="ts">
import TheHeader from '@/components/TheHeader.vue'
import TheFooter from '@/components/TheFooter.vue'
</script>

<template>
  <div id="app">
    <the-header />
    <div class="main-content">
      <router-view />
    </div>
    <the-footer />
  </div>
</template>

<style>
#app {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.main-content {
  flex-grow: 1;
}
</style>
