<template>
      <q-layout view="lHh lp lFf"container style="height: 100px" >
      <q-header   class="bg-primary " elevated >
        <q-toolbar>
          <q-toolbar-title style="margin-left: 20%;">C & W</q-toolbar-title>
        </q-toolbar>
        <q-tabs v-model="tab">
          <q-tab name="home" label="Home" />
          <q-tab name="present-list" label="Present List" />
          <q-tab name="event-location" label="Event Location" />
        </q-tabs>
      </q-header>
    </q-layout>
  
  
</template>

<script setup>

</script>

<style></style>