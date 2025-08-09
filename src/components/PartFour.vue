<script setup>
const usersList = [
  {
    id: 23,
    gender: 'female',
    firstname: 'Emily',
    lastname: 'Parker',
    age: 24,
    account: {
      premium: true,
      avatar: {
        url: 'https://res.cloudinary.com/lereacteur-apollo/image/upload/v1706536025/RNCP31114/cours-vue/exos-sem-3/conditionnal-display-emily_py1pu1.jpg',
      },
    },
  },
  {
    id: 54,
    gender: 'male',
    firstname: 'Marcus',
    lastname: 'Bennett',
    age: 38,
    account: {
      premium: false,
    },
  },
]
</script>

<template>
  <section>
    <div v-for="user in usersList" :key="user.id">
      <div>
        <img v-if="user.account.avatar" :src="user.account.avatar.url" alt="Image de profil" />
        <font-awesome-icon v-if="!user.account.avatar" :icon="['fas', 'user']" />
      </div>
      <div>
        <p>{{ user.firstname }}</p>
        <p>{{ user.lastname }}</p>
        <p>{{ user.age }} ans</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  display: flex;
  gap: 20px;
}

img {
  width: 100px;
  height: 140px;
  object-position: center;
  object-fit: cover;
  border-radius: 5px;
}

section > div {
  display: flex;
  gap: 15px;
  border: 2px solid black;
  padding: 10px;
  border-radius: 10px;
  width: 250px;
}

section > div div:last-of-type {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 10px;
}

svg {
  font-size: 140px;
}
</style>
