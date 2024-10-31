<template>
    <div>
      <button @click="toggleComponent">Switch Component</button>
      <keep-alive>
        <component :is="currentComponent"></component>
      </keep-alive>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue'
  import ComponentA from './ComponentA.vue'
  import ComponentB from './ComponentB.vue'
  
  export default {
    components: { ComponentA, ComponentB },
    setup() {
      const currentComponent = ref('ComponentA')
      const toggleComponent = () =>
        (currentComponent.value = currentComponent.value === 'ComponentA' ? 'ComponentB' : 'ComponentA')
      return { currentComponent, toggleComponent }
    },
  }
  </script>
  