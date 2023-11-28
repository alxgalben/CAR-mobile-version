<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div>
      <Datepicker v-model="date" :format="format"
      :min-date="new Date()"
      :max-date="maxDate" 
      prevent-min-max-navigation
      :enable-time-picker="false"
      placeholder="Selecteaza data de preluare"
      />

      <Datepicker v-model="time" :start-time="startTime" 
      time-picker  
      minutes-increment="15" 
      minutes-grid-increment="15"
      placeholder="Selecteaza ora de preluare"
      style="margin-top: 10px;"
      />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import Datepicker from '@vuepic/vue-datepicker';
  import '@vuepic/vue-datepicker/dist/main.css';
  
  const date = ref(new Date());
  const startTime = ref({ hours: 0, minutes: 0 });

  const time = ref({
    hours: new Date().getHours(),
    minutes: new Date().getMinutes()
  });

  const format = (date) => {
  const day = date.getDate();
  const month = date.getMonth() + 1;
  const year = date.getFullYear();

  return `${day}/${month}/${year}`;
}

  </script>
  