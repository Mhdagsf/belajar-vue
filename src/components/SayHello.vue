<script setup>
import { computed, reactive, ref } from 'vue';

const person = reactive({
  firstName: '',
  lastName: '',
});
function sayHello() {
  // SALAH: Manipulasi DOM langsung
  person.firstName = document.getElementById('firstName').value;
  person.lastName = document.getElementById('lastName').value;
}
const fullName = computed((oldName) => {
  console.log(`Change old name ${oldName}`); // <-- Salah, seharusnya backticks (`)
  return `${person.firstName} ${person.lastName}`;
});
const counter = ref(0);

function increment() {
  console.log('increment called');
  counter.value++;
}

function changeFirstName(event) {
  person.firstName = event.target.value;
}
function changeLastName(event) {
  person.lastName = event.target.value;
}
</script>

<template>
  <div>
    <form>
      <button v-on:click="increment">Say Hello</button> <br />
      <input
        placeholder="first name"
        type="text"
        id="firstName"
        @input="changeFirstName"
      />
      <br />
      <input
        placeholder="last name"
        type="text"
        id="lastName"
        @input="changeLastName"
      />
      <br />
      <button v-on:click.prevent="sayHello">Say Hello</button>
    </form>
  </div>
  <h1>Hello {{ fullName }}</h1>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
