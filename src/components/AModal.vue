<script setup>
import AButton from "./AButton.vue";
const props = defineProps(["modalActive"]);

const emit = defineEmits(["close"]);

function close() {
  emit("close");
}
</script>

<template>
  <transition name="modal-animation">
    <div v-if="modalActive" class="modal">
      <transition name="modal-animation-inner">
        <div v-if="modalActive" class="modal-inner">
          <slot></slot>
          <AButton @click="close" :title="'Close'" />
        </div>
      </transition>
    </div>
  </transition>
</template>

<style scoped>
.modal {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100vw;
  position: fixed;
  top: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.5);
}

.modal-inner {
  position: relative;
  max-width: 32rem;
  width: 80%;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
  background-color: #fff;
  border-radius: 10px;
  padding: 1rem 2rem;
  color: black;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}
</style>
