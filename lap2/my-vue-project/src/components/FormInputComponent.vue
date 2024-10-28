<template>
    <div>
      <!-- Text Input -->
      <h3>Text Input</h3>
      <p>Message: {{ message }}</p>
      <input v-model="message" placeholder="Enter a message" />
  
      <!-- Multiline Text -->
      <h3>Multiline Text</h3>
      <p>Multiline Message: {{ multilineMessage }}</p>
      <textarea v-model="multilineMessage" placeholder="Add multiple lines"></textarea>
  
      <!-- Checkbox -->
      <h3>Single Checkbox</h3>
      <input type="checkbox" v-model="checked" />
      <label>Checked: {{ checked }}</label>
  
      <!-- Multiple Checkboxes -->
      <h3>Multiple Checkboxes</h3>
      <p>Checked names: {{ checkedNames }}</p>
      <input type="checkbox" id="jack" value="Jack" v-model="checkedNames" />
      <label for="jack">Jack</label>
      <input type="checkbox" id="john" value="John" v-model="checkedNames" />
      <label for="john">John</label>
      <input type="checkbox" id="mike" value="Mike" v-model="checkedNames" />
      <label for="mike">Mike</label>
  
      <!-- Radio -->
      <h3>Radio Buttons</h3>
      <p>Picked: {{ picked }}</p>
      <input type="radio" id="one" value="One" v-model="picked" />
      <label for="one">One</label>
      <input type="radio" id="two" value="Two" v-model="picked" />
      <label for="two">Two</label>
  
      <!-- Single Select -->
      <h3>Single Select</h3>
      <p>Selected: {{ selected }}</p>
      <select v-model="selected">
        <option disabled value="">Please select one</option>
        <option>A</option>
        <option>B</option>
        <option>C</option>
      </select>
  
      <!-- Multiple Select -->
      <h3>Multiple Select</h3>
      <p>Selected Options: {{ selectedOptions }}</p>
      <select v-model="selectedOptions" multiple>
        <option>A</option>
        <option>B</option>
        <option>C</option>
      </select>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    setup() {
      const message = ref('');
      const multilineMessage = ref('');
      const checked = ref(false);
      const checkedNames = ref([]);
      const picked = ref('');
      const selected = ref('');
      const selectedOptions = ref([]);
  
      return {
        message,
        multilineMessage,
        checked,
        checkedNames,
        picked,
        selected,
        selectedOptions
      };
    }
  };
  </script>
  
  <style scoped>
  h3 {
    color: #333;
    margin-top: 20px;
  }
  </style>
  