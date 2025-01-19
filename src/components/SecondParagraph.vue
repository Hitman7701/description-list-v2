<script setup>
const props = defineProps({
  firstname: String,
  firstHooby: String,
  secondHobby: String,
})
</script>

<template>
  <p>Outside of work, {{ firstname }} likes to {{ firstHooby }} and {{ secondHobby }}.</p>
</template>
