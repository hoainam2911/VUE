<template>
    <div>
      <button @click="openModal">Open Modal</button>
      <teleport to="body">
        <div v-if="modalOpen" class="modal">
          <p>Teleported Modal</p>
          <button @click="closeModal">Close</button>
        </div>
      </teleport>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue'
  export default {
    setup() {
      const modalOpen = ref(false)
      const openModal = () => (modalOpen.value = true)
      const closeModal = () => (modalOpen.value = false)
      return { modalOpen, openModal, closeModal }
    },
  }
  </script>
  
  <style scoped>
  .modal {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    padding: 20px;
    background-color: white;
    border: 1px solid #ccc;
    z-index: 1000;
  }
  </style>
  