<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div>
      <Datepicker v-model="date" 
      range multi-calendars 
      :min-date="new Date()"
      :max-date="maxDate" 
      prevent-min-max-navigation
      placeholder="Selecteaza data de preluare si predare"
      />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import Datepicker from '@vuepic/vue-datepicker';
  import '@vuepic/vue-datepicker/dist/main.css';
  
  const date = ref();
  </script>
  