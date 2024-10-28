<template>
    <div>
      <p>
        Đặt một câu hỏi có/không:
        <input v-model="question" :disabled="loading" />
      </p>
      <p>Câu trả lời: {{ answer }}</p>
    </div>
  </template>
  
  <script setup>
  import { ref, watch } from 'vue';
  
  const question = ref(''); 
  const answer = ref('Câu hỏi thường có dấu chấm hỏi. ;-)'); 
  const loading = ref(false);
  
  // Sử dụng watch để theo dõi biến question
  watch(question, async (newQuestion) => {
    // Kiểm tra nếu câu hỏi chứa dấu '?'
    if (newQuestion.includes('?')) {
      loading.value = true;
      answer.value = 'Đang suy nghĩ...';
  
      try {
        const response = await fetch('https://yesno.wtf/api');
        const data = await response.json();
        answer.value = data.answer;
      } catch (error) {
        answer.value = 'Lỗi! Không thể truy cập API. ' + error;
      } finally {
        loading.value = false;
      }
    }
  });
  </script>
  
  <style scoped>
  input {
    margin-top: 10px;
    padding: 8px;
    font-size: 1em;
  }
  </style>
  