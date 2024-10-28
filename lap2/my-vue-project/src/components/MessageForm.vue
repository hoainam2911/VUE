<template>
    <div>
      <form @submit.prevent="onSubmit">
        <input type="text" v-model="message" placeholder="Type something..." />
        <button type="submit">Submit</button>
      </form>
      <p>{{ submittedMessage }}</p>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const message = ref('');
      const submittedMessage = ref('');
  
      function onSubmit() {
        submittedMessage.value = "Form submitted with message: " + message.value;
        message.value = '';
      }
  
      return {
        message,
        submittedMessage,
        onSubmit,
      };
    },
  };
  </script>
  