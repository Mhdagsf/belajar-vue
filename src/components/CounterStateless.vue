<script setup>
const { counter, name, increment } = defineProps({
  counter: Number,
  name: String,
  increment: Number,
});
const emits = defineEmits(['click']);

function buttonClick() {
  emits('click', increment);
}
</script>

<template>
  <h1>Counter: {{ name }} : {{ counter }}</h1>
  <button @click="emits('click', increment)">increment {{ name }}</button>
</template>

<style></style>
