<script setup lang="ts">
defineProps({
  title: {
    default: 'Sotib olish',
    type: String
  },
  btn_type: {
    type: String,
    default: 'button',
    validator: function (value: any) {
      return ['button', 'submit', 'reset'].includes(value)
    }
  },
  padding_top: {
    default: '16px'
  },
  padding_bottom: {
    default: '14px'
  },
  padding_left: {
    default: '78px'
  },
  padding_right: {
    default: '72px'
  }
})
</script>

<template>
  <button
    type="button"
    :style="{
      'padding-top': padding_top,
      'padding-bottom': padding_bottom,
      'padding-left': padding_left,
      'padding-right': padding_right
    }"
    class="base-button"
  >
    {{ title }}
  </button>
</template>

<style scoped>
.base-button {
  font-weight: 900;
  color: white;
  background-color: var(--text-red);
  border-radius: 12px;
  text-transform: uppercase;
  border: none;
  font-size: 18px;
  line-height: 27px;
  cursor: pointer;
}
</style>
