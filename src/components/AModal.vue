<script>
export default {
  props: ["modalActive"],
  setup(props, { emit }) {
    const close = () => {
      emit("close");
    };

    return { close };
  },
};
</script>

<template>
  <transition name="modal-animation">
    <div v-if="modalActive" class="modal">
      <transition name="modal-animation-inner">
        <div v-if="modalActive" class="modal-inner">
          <slot></slot>
          <button @click="close">Close</button>
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
  max-width: 640px;
  width: 80%;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
  background-color: #fff;
  padding: 64px 16px;
  color: black;
}
</style>

<!-- <script setup>
import { ref } from "vue";

const props = defineProps(["isLogin"]);
const visible = ref(false);

const showModal = () => {
  visible.value = true;
};

const handleOk = (e) => {
  console.log(e);
  visible.value = false;
};

const title = props.isLogin ? "Login" : "Signup";
</script> -->
