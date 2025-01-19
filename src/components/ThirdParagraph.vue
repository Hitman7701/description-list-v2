<script setup>
const props = defineProps({
  gender: String,
  petName: String,
  petAge: Number,
  petSpecie: String,
})
</script>

<template>
  <p>
    At home, {{ gender === 'female' ? 'her' : 'his' }} lively companion is {{ petName }} a
    {{ petAge }}-years-old {{ petSpecie }}.
  </p>
</template>
