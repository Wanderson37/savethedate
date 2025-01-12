<template>
    Our day is coming in
    <div class="countdown">
      <div class="countdown-item">
        <span class="count">{{ days }}</span>
        <span class="label">Days</span>
      </div>
      <div class="countdown-item">
        <span class="count">{{ hours }}</span>
        <span class="label">Hours</span>
      </div>
      <div class="countdown-item">
        <span class="count">{{ minutes }}</span>
        <span class="label">Minutes</span>
      </div>
      <div class="countdown-item">
        <span class="count">{{ seconds }}</span>
        <span class="label">Seconds</span>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue';
  
  const targetDate = new Date('2025-06-24T19:00:00'); // Altere para a data do seu evento
  const days = ref(0);
  const hours = ref(0);
  const minutes = ref(0);
  const seconds = ref(0);
  
  const updateCountdown = () => {
    const now = new Date();
    const difference = targetDate - now;
  
    if (difference > 0) {
      days.value = Math.floor(difference / (1000 * 60 * 60 * 24));
      hours.value = Math.floor((difference / (1000 * 60 * 60)) % 24);
      minutes.value = Math.floor((difference / (1000 * 60)) % 60);
      seconds.value = Math.floor((difference / 1000) % 60);
    } else {
      days.value = 0;
      hours.value = 0;
      minutes.value = 0;
      seconds.value = 0;
    }
  };
  
  onMounted(() => {
    updateCountdown();
    setInterval(updateCountdown, 1000); // Atualiza o contador a cada segundo
  });
  </script>
  
  <style>
  .countdown {
    display: flex;
    justify-content: center;
    gap: 1rem;
    font-family: 'Arial', sans-serif;
    text-align: center;
  }
  
  .countdown-item {
    background: #fff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    min-width: 80px;
  }
  
  .count {
    display: block;
    font-size: 2rem;
    font-weight: bold;
    color: #333;
  }
  
  .label {
    font-size: 1rem;
    color: #666;
  }
  </style>
  