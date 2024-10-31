<template>
    <suspense>
      <template #default>
        <AsyncComponent />
      </template>
      <template #fallback>
        <p>Loading async component...</p>
      </template>
    </suspense>
  </template>
  
  <script>
  import { defineAsyncComponent } from 'vue'
  const AsyncComponent = defineAsyncComponent(() =>
    new Promise((resolve) => {
      setTimeout(() => {
        resolve(import('./AsyncComponent.vue'))
      }, 2000)
    })
  )
  
  export default {
    components: { AsyncComponent },
  }
  </script>
  