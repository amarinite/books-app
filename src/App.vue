<script setup>
import { RouterView } from "vue-router";
import NavBar from "./components/NavBar.vue";
import Container from "./components/Container.vue";
</script>

<template>
  <main>
    <NavBar />
    <Container> <RouterView /></Container>
  </main>
</template>

<style scoped></style>
