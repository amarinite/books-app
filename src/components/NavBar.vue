<script setup>
import AModal from "./AModal.vue";
import AButton from "./AButton.vue";
import { ref } from "vue";
import { RouterLink } from "vue-router";

const modalActive = ref(false);

const toggleModal = () => {
  modalActive.value = !modalActive.value;
};
</script>

<template>
  <header>
    <div class="left-side">
      <h1><router-link to="/">The Book Archive</router-link></h1>
      <router-link to="/books">My books</router-link>
      <a href="#">Stats</a>
      <a href="#">Reading Journal</a>
    </div>
    <div class="right-side">
      <input class="searchbar" type="text" placeholder="Search a book..." />
      <i></i>
      <AModal @close="toggleModal" :modalActive="modalActive">
        <h2>Log a book</h2>
        <form>
          <label for="title">Title</label>
          <input type="text" name="title" />
          <label for="author">Author</label>
          <input type="text" name="author" />
          <label for="finished" name="finished">Finished on</label>
          <input type="date" />
        </form>
      </AModal>
      <AButton @click="toggleModal" :title="'Log a book!'" />
      <div class="user-corner">
        <p>Username</p>
        <img
          src="https://static.vecteezy.com/system/resources/previews/008/442/086/original/illustration-of-human-icon-user-symbol-icon-modern-design-on-blank-background-free-vector.jpg"
          alt=""
        />
      </div>
    </div>
  </header>
</template>

<style scoped>
header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 4rem;
  padding: 0 1.8rem;
  background-color: #472d30;
  color: #fdfffc;
  /* #FDFFFC */
  /* #011627 */
  /* #2D4744 */
}

header div {
  display: flex;
  align-items: center;
}

.left-side {
  gap: 4rem;
}

.left-side a {
  color: #fdfffc;
  text-decoration: none;
}
.searchbar {
  border: none;
  padding: 0.5rem 1rem 0.2rem 1rem;
  color: #fdfffc;
  width: 20rem;
  font-size: 15px;
  background: none;
  border-bottom: 1px solid #fdfffc;
}

.right-side {
  gap: 3rem;
}

.user-corner p {
  font-size: 16px;
}

.user-corner img {
  height: 30px;
  width: 30px;
  border: 1px solid #fdfffc;
  border-radius: 50%;
  margin-left: 1rem;
}

form {
  display: flex;
  flex-direction: column;
}
</style>
