<script setup>
import AModal from "./AModal.vue";
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
      <input type="text" placeholder="Search a book..." />
      <i></i>
      <AModal @close="toggleModal" :modalActive="modalActive">
        <div class="modal-content">
          <h3>demo</h3>
        </div>
      </AModal>
      <button @click="toggleModal">Log a book!</button>
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
.right-side input {
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
