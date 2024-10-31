<template>
    <div>
      <button @click="toggleShow">Toggle Box</button>
      <transition name="fade">
        <div v-if="showBox" class="box">Transitioned Box</div>
      </transition>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue'
  export default {
    setup() {
      const showBox = ref(false)
      const toggleShow = () => (showBox.value = !showBox.value)
      return { showBox, toggleShow }
    },
  }
  </script>
  
  <style scoped>
  .fade-enter-active, .fade-leave-active {
    transition: opacity 0.5s;
  }
  .fade-enter, .fade-leave-to {
    opacity: 0;
  }
  .box {
    width: 100px;
    height: 100px;
    background-color: lightblue;
    margin: 10px 0;
  }
  </style>
  