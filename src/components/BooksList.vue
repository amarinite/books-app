<script setup>
const { books } = defineProps(["books"]);
</script>

<template>
  <div class="books">
    <div class="book" v-for="book in books" :key="index">
      <img :src="book.image" alt="" />
      <p>{{ book.rating }}</p>
      <p>{{ book.date }}</p>
    </div>
  </div>
</template>

<style scoped>
.books {
  margin-top: 3rem;
  display: grid;
  grid-template-columns: repeat(6, 1fr);
}

.book img {
  width: 10rem;
  border-radius: 5px;
  box-shadow: 1px 1px 4px #899e9c;
}
</style>
