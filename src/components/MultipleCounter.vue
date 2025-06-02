<script setup>
import { ref } from 'vue';
import Counter from './Counter.vue';
import CounterStateless from './CounterStateless.vue';

const counter = ref(0);

function increment(value) {
  counter.value += value;
}
</script>

<template>
  <Counter name="Bagas" initial-count="10" />
  <Counter name="Agis" initial-count="2 0" />

  <CounterStateless
    name="Joko"
    :counter="counter"
    :increment="1"
    v-on:click="increment"
  />
  <CounterStateless
    name="Budi"
    :counter="counter"
    :increment="2"
    @click="increment"
  />
</template>
