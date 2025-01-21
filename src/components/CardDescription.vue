<script setup>
const props = defineProps({
  personInfos: Object,
})

import FirstParagraph from './FirstParagraph.vue'
import Title from './Title.vue'
import SecondParagraph from './SecondParagraph.vue'
import ThirdParagraph from './ThirdParagraph.vue'
</script>

<template>
  <div class="card">
    <img
      src="https://res.cloudinary.com/lereacteur-apollo/image/upload/v1704967000/RNCP31114/cours-vue/exo-sem-1/mystery-person_bueack.jpg"
      alt="user"
    />
    <Title
      :firstname="personInfos.firstname"
      :lastname="personInfos.lastname"
      :gender="personInfos.gender"
    />
    <FirstParagraph :gender="personInfos.gender" :age="personInfos.age" :job="personInfos.job" />
    <SecondParagraph
      :firstname="personInfos.firstname"
      :firstHobby="personInfos.hobbies[1]"
      :secondHobby="personInfos.hobbies[1]"
    />
    <ThirdParagraph
      :gender="personInfos.gender"
      :petName="personInfos.pet.name"
      :petAge="personInfos.pet.age"
      :petSpecie="personInfos.pet.species"
    />
    <font-awesome-icon :icon="['fas', 'heart']" />
  </div>
</template>

<style scoped>
.card {
  padding: 10px;
  background-color: #eeeeee;
  border-radius: 5px;
  box-shadow: 0 0 7px v-bind('personInfos.favoriteColor');
  display: flex;
  flex-direction: column;
  flex: 1;
  justify-content: space-between;
}

img {
  width: 100%;
  aspect-ratio: 16/10;
  object-fit: cover;
  object-position: top;
  border-radius: 5px;
}

svg {
  align-self: flex-end;
  font-size: 26px;
  color: grey;
  cursor: pointer;
}

@media (max-width: 1250px) {
  .card {
    flex: none;
    width: 290px;
    margin-bottom: 10px;
  }
}
</style>
