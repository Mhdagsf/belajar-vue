<script setup>
const items = [
  {
    id: 1,
    text: 'Learn vue 3',
    done: true,
  },
  {
    id: 2,
    text: 'Learn vue Router',
    done: false,
  },
  {
    id: 3,
    text: 'Learn vue Pinia',
    done: false,
  },
  {
    id: 4,
    text: 'Learn vue Pinia 2 ',
    done: false,
  },
];
</script>

<template>
  <h1>Todo List</h1>
  <template v-for="item in items">
    <ul :key="item.id" v-if="item.done == false">
      <li v-for="(value, key) in item">{{ key }}:{{ value }}</li>
    </ul>
  </template>

  <h1 v-for="i in 10">Hello {{ i }}</h1>
</template>

<style scoped></style>
