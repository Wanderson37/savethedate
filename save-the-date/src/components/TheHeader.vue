<template>
  <div class="q-pa-md">
    <q-layout >
      <q-header class="bg-primary" reveal elevated>
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
  </div>
</template>

<script setup>

</script>

<style></style>