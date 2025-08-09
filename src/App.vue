<script setup>
import PartFour from './components/PartFour.vue'
import PartOne from './components/PartOne.vue'
import PartThree from './components/PartThree.vue'
import PartTwo from './components/PartTwo.vue'
</script>

<template>
  <main class="container">
    <h1>Conditional display</h1>
    <div>
      <PartOne />
      <PartTwo />
      <PartThree />
      <PartFour />
    </div>
  </main>
</template>

<style scoped>
main {
  height: 100vh;
  padding: 50px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
}

h1 {
  font-size: 45px;
  font-weight: bold;
}

main > div {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}
</style>
