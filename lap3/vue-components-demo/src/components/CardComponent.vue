<template>
    <div class="card">
      <h2><slot name="title" /></h2>
      <slot />
    </div>
  </template>
  
  <style scoped>
  .card {
    border: 1px solid #ccc;
    padding: 16px;
    border-radius: 8px;
    margin-top: 16px;
  }
  </style>
  