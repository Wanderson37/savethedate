<template>
  <div class="map-container">
    <!-- Mapa do Google -->
    <div class="map" ref="map"></div>

    <!-- Endereço -->
    <div class="address">
      <h2>Event Location</h2>
      <p>{{ address }}</p>
    </div>
  </div>
  <br />
</template>

<script setup>
/* global google */
import { ref, onMounted } from 'vue'
const map = ref(null)
onMounted(() => {
  new window.google.maps.Map(map.value, {
    center: { lat: -2.953697088106651, lng: -60.09786083612656 }, // Coordenadas de exemplo
    zoom: 15,
  })
})
const address = 'Av. do Pontal - Tarumã Açu, Manaus - AM' // Altere o endereço conforme necessário
const mapRef = ref(null)

// Função para inicializar o mapa
const initMap = () => {
  const map = new google.maps.Map(mapRef.value, {
    center: { lat: -2.953697088106651, lng: -60.09786083612656 }, // Coordenadas de exemplo
    zoom: 15,
  })

  // Marcador no mapa
  new google.maps.Marker({
    position: { lat: -23.55052, lng: -46.633308 }, // Coordenadas de exemplo
    map: map,
    title: 'Event Location',
  })
}

onMounted(() => {
  initMap() // Inicializa o mapa ao montar o componente
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
