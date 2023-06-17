<script setup>
const props = defineProps(["title", "type"]);
</script>

<template>
  <button :class="type === 'main' ? 'main' : 'secondary'">{{ title }}</button>
</template>

<style scoped>
button {
  border: none;
  background-color: #fdaa10;
  padding: 0.5rem 1rem;
  font-weight: bold;
  font-size: 15px;
  border-radius: 10px;
  cursor: pointer;
}

button:hover {
  background-color: #ffbd41;
}
</style>
