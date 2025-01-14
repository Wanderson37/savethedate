<template>
  <TheHeader />
  <div class="day-count">
    <DayCount />
      </div>
      <br>
  <TheLocation />
  <br>
</template>

<script setup>
import DayCount from '@/components/DayCount.vue';
import TheLocation from '@/components/TheLocation.vue';
import TheHeader from '@/components/TheHeader.vue';
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