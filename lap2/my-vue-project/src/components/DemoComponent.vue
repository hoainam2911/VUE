<!-- src/components/DemoComponent.vue -->
<template>
  <div>
    <h2>This is the Demo Component</h2>
    <button @click="increment">You clicked me {{ count }} times.</button>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0);

function increment() {
  count.value++;
}
</script>

<style scoped>
h2 {
  color: #42b983;
}
</style>
