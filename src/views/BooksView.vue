<script setup>
const books = [
  {
    image:
      "https://images-na.ssl-images-amazon.com/images/S/compressed.photo.goodreads.com/books/1607462569i/53152636.jpg",
    rating: "⭐⭐⭐⭐⭐",
    date: "Jun 13",
  },
  {
    image:
      "https://images-na.ssl-images-amazon.com/images/S/compressed.photo.goodreads.com/books/1683027004i/146582923.jpg",
    rating: "⭐⭐⭐⭐⭐",
    date: "Jun 13",
  },
  {
    image:
      "https://i.gr-assets.com/images/S/compressed.photo.goodreads.com/books/1665211641l/62906919.jpg",
    rating: "⭐⭐⭐⭐⭐",
    date: "Jun 13",
  },
  {
    image:
      "https://www.raigverdeditorial.cat/wp-content/uploads//2021/07/Portada_DIABLE-A-LA-CREU_web.jpg",
    rating: "⭐⭐⭐⭐⭐",
    date: "Jun 13",
  },
  {
    image:
      "https://images-na.ssl-images-amazon.com/images/S/compressed.photo.goodreads.com/books/1607462569i/53152636.jpg",
    rating: "⭐⭐⭐⭐⭐",
    date: "Jun 13",
  },
  {
    image:
      "https://images-na.ssl-images-amazon.com/images/S/compressed.photo.goodreads.com/books/1607462569i/53152636.jpg",
    rating: "⭐⭐⭐⭐⭐",
    date: "Jun 13",
  },
  {
    image:
      "https://images-na.ssl-images-amazon.com/images/S/compressed.photo.goodreads.com/books/1607462569i/53152636.jpg",
    rating: "⭐⭐⭐⭐⭐",
    date: "Jun 13",
  },
  {
    image:
      "https://images-na.ssl-images-amazon.com/images/S/compressed.photo.goodreads.com/books/1607462569i/53152636.jpg",
    rating: "⭐⭐⭐⭐⭐",
    date: "Jun 13",
  },
  {
    image:
      "https://images-na.ssl-images-amazon.com/images/S/compressed.photo.goodreads.com/books/1607462569i/53152636.jpg",
    rating: "⭐⭐⭐⭐⭐",
    date: "Jun 13",
  },

  {
    image:
      "https://images-na.ssl-images-amazon.com/images/S/compressed.photo.goodreads.com/books/1607462569i/53152636.jpg",
    rating: "⭐⭐⭐⭐⭐",
    date: "Jun 13",
  },
  {
    image:
      "https://images-na.ssl-images-amazon.com/images/S/compressed.photo.goodreads.com/books/1607462569i/53152636.jpg",
    rating: "⭐⭐⭐⭐⭐",
    date: "Jun 13",
  },
];
</script>

<template>
  <div class="top-content">
    <h1>My Book Collection</h1>
    <div class="filters">
      <p class="filter-by">Filter by...</p>
      <p>G</p>
      <p>L</p>
    </div>
  </div>
  <div class="books">
    <div class="book" v-for="book in books" :key="index">
      <img :src="book.image" alt="" />
      <p>{{ book.rating }}</p>
      <p>{{ book.date }}</p>
    </div>
  </div>
</template>

<style scoped>
.top-content,
.filters {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
}

.filters {
  gap: 2rem;
}

/* .filters p {
  background-color: #2d4744;
} */

.top-content h1 {
  color: #2d4744;
}

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
