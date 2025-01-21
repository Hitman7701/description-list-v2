<script setup>
const personsList = [
  {
    gender: 'female',
    firstname: 'Emily',
    lastname: 'Parker',
    age: 24,
    job: 'teacher',
    hobbies: ['read books', 'go hiking'],
    pet: {
      name: 'Whiskers',
      age: 2,
      species: 'ferret',
    },
    favoriteColor: 'red',
  },
  {
    gender: 'male',
    firstname: 'Marcus',
    lastname: 'Bennett',
    age: 38,
    job: 'architect',
    hobbies: ['watch bird', 'play chess'],
    pet: {
      name: 'Nala',
      age: 6,
      species: 'dog',
    },
    favoriteColor: 'blue',
  },
  {
    gender: 'female',
    firstname: 'Sophia',
    lastname: 'Rodriguez',
    age: 31,
    job: 'environmental scientist',
    hobbies: ['play guitar', 'bake cakes'],
    pet: {
      name: 'Paws',
      age: 3,
      species: 'cat',
    },
    favoriteColor: 'orange',
  },
  {
    gender: 'male',
    firstname: 'Oliver',
    lastname: 'Hughes',
    age: 56,
    job: 'carpenter',
    hobbies: ['paint', 'ride horses'],
    pet: {
      name: 'Bubble',
      age: 4,
      species: 'snake',
    },
    favoriteColor: 'purple',
  },
]

import CardDescription from './components/CardDescription.vue'
</script>

<template>
  <main>
    <h1>Description list</h1>
    <div>
      <CardDescription :personInfos="personsList[0]" />
      <CardDescription :personInfos="personsList[1]" />
      <CardDescription :personInfos="personsList[2]" />
      <CardDescription :personInfos="personsList[3]" />
    </div>
  </main>
</template>

<style scoped>
main {
  min-height: 100vh;
  width: 100vw;
}

main > div {
  display: flex;
  gap: 10px;
  margin: 0 auto;
  padding: 0 30px;
}

@media (max-width: 1250px) {
  main > div {
    flex-wrap: wrap;
    justify-content: center;
  }
}
</style>
