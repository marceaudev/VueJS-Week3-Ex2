<script setup>
import { ref } from 'vue'

const money = ref(0)
</script>

<template>
  <section>
    <p v-if="money === 0">😱 Mon porte monnaie est vide</p>
    <p v-else-if="money === 1">Mon premier euros 🤩</p>
    <p v-else-if="money > 30">🍾 Ca y est je suis riche !! 🍾</p>
    <p v-else-if="money > 10">Yes, plus de 10 €</p>
    <p>{{ money }} €</p>
    <div>
      <button @click="money++">Ajouter 1€</button>
      <button @click="money += 5">Ajouter 5€</button>
    </div>
  </section>
</template>

<style scoped>
section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 25px;
}

p:first-of-type {
  color: coral;
  font-size: 20px;
  font-weight: bold;
}

p:last-of-type {
  font-weight: bold;
  font-size: 20px;
}

section > div {
  display: flex;
  gap: 25px;
}

button {
  background: transparent;
  border: 2px solid black;
  padding: 10px;
  border-radius: 10px;
  font-size: 16px;
}
</style>
