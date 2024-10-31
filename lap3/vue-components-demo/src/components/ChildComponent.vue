<template>
    <div>
      <h3>Hello, {{ name }}!</h3>
      <button @click="$emit('childClicked')">Click Me!</button>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      name: {
        type: String,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  /* Thêm CSS tại đây nếu cần */
  </style>
  