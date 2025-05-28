<script setup>
console.info("Hello Vue");

const hello = "<h1>Hello vue</h1>".toUpperCase(); // Perhatikan penulisan nama variabel yang lebih konsisten

const data = {
  class: "hello",
  id: "hello",
};
const buttonDisabled = true;
</script>

<template>
  <h1 v-bind="data">{{ hello }}</h1>
  <div :class="data.class" v-html="hello"></div>

  <button :disabled="buttonDisabled">This is button</button>
</template>

<style scoped>
.hello {
  color: green;
}
</style>
