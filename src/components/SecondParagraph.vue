<script setup>
const props = defineProps({
  firstname: String,
  firstHobby: String,
  secondHobby: String,
})
</script>

<template>
  <p>Outside of work, {{ firstname }} likes to {{ firstHobby }} and {{ secondHobby }}.</p>
</template>
