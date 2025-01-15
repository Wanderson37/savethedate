<template>
  <q-layout>
  <TheHeader />
  <ThePhoto />
   </q-layout>
  <DayCount />      
  <TheLocation />
 
</template>

<script setup>
import DayCount from '@/components/DayCount.vue';
import TheLocation from '@/components/TheLocation.vue';
import TheHeader from '@/components/TheHeader.vue';
import ThePhoto from '@/components/ThePhoto.vue';

</script>
<style>

</style>