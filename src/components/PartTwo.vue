<script setup>
import { ref } from 'vue'

const isLiked = ref(false)
</script>

<template>
  <section>
    <font-awesome-icon
      :style="{ color: 'green' }"
      :icon="['fas', 'thumbs-up']"
      v-show="isLiked"
      @click="isLiked = false"
    />
    <font-awesome-icon
      :style="{ color: 'red' }"
      :icon="['fas', 'thumbs-down']"
      v-show="!isLiked"
      @click="isLiked = true"
    />
  </section>
</template>

<style scoped>
section {
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 35px;
}

svg {
  transition: 0.2s ease-in-out;
}

svg:hover {
  transform: scale(1.02);
  cursor: pointer;
}
</style>
