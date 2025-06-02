<script setup>
import { reactive } from 'vue';
import ContactForm from './ContactForm.vue';
import ContactList from './ContactList.vue';

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
  <ContactForm v-model="contact" />
  <ContactList
    v-model:name="contact.name"
    v-model:email="contact.email"
    v-model:age="contact.age"
    v-model:type="contact.type"
    v-model:complain="contact.complain"
    v-model:message="contact.message"
  />
</template>

<style scoped>
.hello {
  color: green;
}
</style>
