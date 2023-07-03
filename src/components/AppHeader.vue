<script setup>
import { defineEmits } from "vue";
const emit = defineEmits(['buttonSelete']);
const type = (t) => {
  emit('buttonSelete',t);
}
</script>

<template>
  <header class="head">
    <button type="button" @click="type('Skan')">Skan</button>
    <button type="button" @click="type('All')">All</button>
    <button type="button" @click="type('Create')">Create</button>
  </header>
</template>

<style scoped>

</style>