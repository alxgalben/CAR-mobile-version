<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div>
    <Datepicker v-model="date" 
    :min-date="new Date()"
    :max-date="maxDate" 
    prevent-min-max-navigation
    :enable-time-picker="false"
    placeholder="Selecteaza data de predare"
    />

    <Datepicker v-model="time" time-picker 
      placeholder="Selecteaza ora de predare"
      style="margin-top: 10px;"
      />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import Datepicker from '@vuepic/vue-datepicker';
import '@vuepic/vue-datepicker/dist/main.css';

const date = ref(new Date());
const time = ref({
    hours: new Date().getHours(),
    minutes: new Date().getMinutes()
  });
</script>
