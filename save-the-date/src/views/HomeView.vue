<template>
  <q-layout id="home">
    <TheHeader />
    <ThePhoto />
    <DayCount />
    <TheLocation />
    <TheFooter />
  </q-layout>
</template>

<script setup>
import DayCount from '@/components/DayCount.vue'
import TheLocation from '@/components/TheLocation.vue'
import TheHeader from '@/components/TheHeader.vue'
import ThePhoto from '@/components/ThePhoto.vue'
import TheFooter from '@/components/TheFooter.vue'
import PresentList from '@/components/PresentList.vue'
</script>
<style></style>
