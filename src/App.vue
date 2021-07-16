<template>
  <div class="min-h-screen bg-grey-darker p-8">
    <div class="max-w-sm mx-auto">
      <date-picker v-model="date" :options="{ firstDay: 1 }"></date-picker>
    </div>
  </div>
</template>

<script>
import DatePicker from "./components/DatePicker.vue";

export default {
  components: {
    DatePicker,
  },
  data() {
    return {
      date: "2021-07-16",
    };
  },
};
</script>

<style>
@import "./assets/css/app.css";
</style>
