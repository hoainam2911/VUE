<template>
    <div>
      <label for="input">{{ label }}</label>
      <input
        type="text"
        :value="modelValue"
        @input="$emit('update:modelValue', $event.target.value)"
      />
    </div>
  </template>
  
  <script>
  export default {
    props: {
      modelValue: {
        type: String,
        default: '',
      },
      label: {
        type: String,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  /* Thêm CSS tại đây nếu cần */
  </style>
  