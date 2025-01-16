<template>
  <div class="map-container">
    <!-- Mapa do Google -->
    <div class="map" ref="mapRef"></div>

    <!-- Endereço -->
    <div class="address">
      <h2>Event Location</h2>
      <p style="font-size: 1.5rem">Chácara Bella Vista</p>
      <p>{{ address }}</p>
    </div>
  </div>

  <br />
</template>

<script setup>
/* global google */
import { ref, onMounted } from 'vue'
const address = 'Av. do Pontal - Tarumã Açu, Manaus - AM' // Altere o endereço conforme necessário
const mapRef = ref(null)

const initMap = () => {
  if (mapRef.value) {
    const map = new google.maps.Map(mapRef.value, {
      center: { lat: -2.964747667312622, lng: -60.10305404663086 },
      zoom: 16,
    })

    // Marcador no mapa
    new google.maps.Marker({
      position: { lat: -2.964747667312622, lng: -60.10305404663086 },
      map: map,
      title: 'Event Location',
    })
  } else {
    console.error('mapRef is null')
  }
}

onMounted(() => {
  window.initMap = initMap
  if (window.google) {
    initMap()
  }
})
</script>

<style>
.map-container {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 2rem;
}

.map {
  width: 70%;
  height: 400px;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}

.address {
  width: 25%;
  padding: 1rem;
  background-color: #f9f9f9;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.address h2 {
  margin-bottom: 1rem;
  font-size: 1.5rem;
  color: #333;
}

.address p {
  font-size: 1rem;
  color: #666;
}
</style>
