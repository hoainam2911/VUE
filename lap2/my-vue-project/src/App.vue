<template>
  <div id="app">
    <!-- <h1>Vue Event Handling Demo</h1> -->
    <!-- <CounterButton /> -->
    <!-- <MessageForm /> -->
    <!-- <FormInputComponent /> -->
    <!-- <DemoRef /> -->
    <DemoComponent />
 </div>
</template>

<script>
// import CounterButton from './components/CounterButton.vue';
// import MessageForm from './components/MessageForm.vue';
// import FormInputComponent from './components/FormInputComponent.vue';
// import QuestionAnswer from './components/QuestionAnswer.vue';
// import DemoRef from './components/DemoRef.vue';
import DemoComponent from './components/DemoComponent.vue';
export default {
  components: {
    // CounterButton,
    // MessageForm,
    // FormInputComponent,
    // QuestionAnswer,
    // DemoRef,
    DemoComponent
  },
};
</script>

<style>
#app {
  text-align: center;
}
</style>
