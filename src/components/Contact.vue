<script setup>
import { reactive } from 'vue';

const contact = reactive({
  name: '',
  email: '',
  age: 0,
  type: 'Reguler',
  complain: 'false',
  message: '',
});
</script>

<template>
  <h1>Contact Us</h1>
  <form>
    <div>
      <label for="name"
        >Nama
        <input type="text" id="name" v-model="contact.name" />
      </label>
    </div>
    <div>
      <label for="email"
        >Email
        <input type="text" id="email" v-model="contact.email" />
      </label>
    </div>
    <div>
      <label for="age"
        >Age
        <input type="number" id="age" v-model="contact.age" />
      </label>
    </div>
    <div>
      <label for="type">
        <select name="type" id="type" v-model="contact.type">
          <option value="Reguler">Reguler</option>
          <option value="VIP">VIP</option>
        </select>
      </label>
    </div>
    <div>
      <label for="complain"
        >Complain
        <input type="checkbox" id="complain" v-model="contact.complain" />
      </label>
    </div>
    <div>
      <label for="message"
        >Message
        <textarea
          name="message"
          id="message"
          v-model="contact.message"
        ></textarea>
      </label>
    </div>
  </form>
  <h1>Preview</h1>
  <div>
    <p>Name: {{ contact.name }}</p>
    <p>Email: {{ contact.email }}</p>
    <p>Age: {{ contact.age }}</p>
    <p>Type: {{ contact.type }}</p>
    <p>Complain: {{ contact.complain }}</p>
    <p>Message: {{ contact.message }}</p>
  </div>
</template>

<style scoped>
.hello {
  color: green;
}
</style>
