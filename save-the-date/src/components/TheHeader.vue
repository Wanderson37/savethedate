<template>
  <q-header class="bg-primary" elevated reveal>
    <q-toolbar>
      <q-toolbar-title style="margin-left: 20%">C & W</q-toolbar-title>
    </q-toolbar>
    <q-tabs v-model="tab">
      <q-tab name="home" label="home" @click="scrollTo('home')" />
      <q-tab name="event-location" label="Event Location" @click="scrollTo('location')" />
    </q-tabs>
  </q-header>
</template>

<script setup>
import { ref } from 'vue'

const tab = ref('home')

function scrollTo(id) {
  const element = document.getElementById(id)
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' })
  }
}
</script>

<style></style>
