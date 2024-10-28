<template>
    <div>
      <button @click="increment">Add 1</button>
      <p>Count is: {{ count }}</p>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const count = ref(0);
  
      function increment() {
        count.value++;
      }
  
      return {
        count,
        increment,
      };
    },
  };
  </script>
  