<template>
    <div>
      <button @click="addItem">Add Item</button>
      <transition-group name="list" tag="ul" class="item-list">
        <li v-for="item in items" :key="item" class="list-item">{{ item }}</li>
      </transition-group>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue'
  export default {
    setup() {
      const items = ref(['Item 1', 'Item 2'])
      const addItem = () => items.value.push(`Item ${items.value.length + 1}`)
      return { items, addItem }
    },
  }
  </script>
  
  <style scoped>
  .item-list {
    list-style-type: none;
    padding: 0;
  }
  .list-item {
    margin: 5px 0;
    padding: 5px;
    background-color: #f2f2f2;
  }
  </style>
  