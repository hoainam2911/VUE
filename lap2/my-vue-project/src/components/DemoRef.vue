<template>
    <div>
      <h1>Demo Template Refs</h1>
      <input ref="myInput" placeholder="Nhập gì đó..." />
      <button @click="focusInput">Tập trung vào Input</button>
    </div>
  </template>
  
  <script setup>
  import { useTemplateRef, onMounted } from 'vue';
  
  const myInput = useTemplateRef('myInput');
  
  const focusInput = () => {
    myInput.value.focus(); // Tập trung vào input khi nhấn nút
  };
  
  onMounted(() => {
    console.log('Component đã được gắn.');
  });
  </script>
  