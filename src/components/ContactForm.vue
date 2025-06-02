<script setup>
const model = defineModel({
  type: Object,
  required: true,
});
</script>

<template>
  <h1>Contact Us</h1>
  <form>
    <div>
      <label for="name"
        >Nama
        <input type="text" id="name" v-model="model.name" />
      </label>
    </div>
    <div>
      <label for="email"
        >Email
        <input type="text" id="email" v-model="model.email" />
      </label>
    </div>
    <div>
      <label for="age"
        >Age
        <input type="number" id="age" v-model="model.age" />
      </label>
    </div>
    <div>
      <label for="type">
        <select name="type" id="type" v-model="model.type">
          <option value="Reguler">Reguler</option>
          <option value="VIP">VIP</option>
        </select>
      </label>
    </div>
    <div>
      <label for="complain"
        >Complain
        <input type="checkbox" id="complain" v-model="model.complain" />
      </label>
    </div>
    <div>
      <label for="message"
        >Message
        <textarea
          name="message"
          id="message"
          v-model="model.message"
        ></textarea>
      </label>
    </div>
  </form>
</template>

<style></style>
