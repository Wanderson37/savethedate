<template>
  <router-view />
  <TheHeader />
  <div class="day-count">
    <DayCount />
  </div>
</template>

<script setup>
import DayCount from './components/DayCount.vue';
import TheHeader from './components/TheHeader.vue';

//
</script>
<style>
.daycount {
  display: flex;
  justify-content: center;
  gap: 1rem;
  height: 200rem;
}
</style>