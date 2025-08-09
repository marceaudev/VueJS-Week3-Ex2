<script setup>
import { ref } from 'vue'

const isConnected = ref(false)

const handleConnection = () => {
  isConnected.value = true
}
</script>

<template>
  <section>
    <button v-if="isConnected" @click="isConnected = false">Se déconnecter</button>
    <div v-else>
      <button @click="handleConnection">Se connecter</button>
      <button @click="handleConnection">S'inscrire</button>
    </div>
  </section>
</template>

<style scoped>
section {
  display: flex;
  align-items: center;
  justify-content: center;
}

section > div {
  display: flex;
  gap: 35px;
}

section > div button {
  border: 2px solid green;
  background-color: transparent;
  padding: 10px;
  border-radius: 50px;
  color: green;
  font-size: 16px;
}

section > button {
  border: none;
  background-color: green;
  padding: 10px;
  border-radius: 50px;
  color: white;
  font-size: 16px;
}
</style>
