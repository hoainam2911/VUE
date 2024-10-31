<template>
    <div>
      <h2>Registration</h2>
      <form @submit.prevent="handleSubmit">
        <InputComponent v-model="username" label="Username" />
        <InputComponent v-model="email" label="Email" />
  
        <button type="submit">Register</button>
      </form>
  
      <CardComponent>
        <template #title>
          User Registration
        </template>
        <p>Please fill in your details above.</p>
      </CardComponent>
  
      <ChildComponent :name="username" @childClicked="handleChildClick" />
      
      <component :is="asyncComponent" />
    </div>
  </template>
  
  <script>
  import InputComponent from './InputComponent.vue';
  import ChildComponent from './ChildComponent.vue';
  import CardComponent from './CardComponent.vue';
  
  export default {
    components: {
      InputComponent,
      ChildComponent,
      CardComponent,
    },
    data() {
      return {
        username: '',
        email: '',
        asyncComponent: () => import('./AsyncComponent.vue'),
      };
    },
    methods: {
      handleSubmit() {
        console.log(`Username: ${this.username}, Email: ${this.email}`);
      },
      handleChildClick() {
        alert('Child component clicked!');
      },
    },
  };
  </script>
  
  <style scoped>
  /* Thêm CSS tại đây nếu cần */
  </style>
  