<script setup>
import { ref } from 'vue';

const score = ref(80);
</script>

<template>
  <h1 v-if="score > 90">Yeay cool score {{ score }}</h1>
  <h1 v-else-if="score > 70">Good Score {{ score }}</h1>
  <h1 v-else="score > 70">Ups, Bad Score {{ score }}</h1>
</template>

<style scoped></style>
