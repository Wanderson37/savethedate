<template>
    <div :class="['header', { scrolled: isScrolled }]">
      <div class="monogram">Carolina e Wanderson</div>
      <nav>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">Presents List</a></li>
          <li><a href="#">Event location</a></li>
        </ul>
      </nav>
    </div>
    <img src="/couple.jpg" alt="Wedding couple" />
  </template>
  
  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue';
  
  const isScrolled = ref(false);
  
  const handleScroll = () => {
    isScrolled.value = window.scrollY > 50;
  };
  
  onMounted(() => {
    window.addEventListener('scroll', handleScroll);
  });
  
  onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll);
  });
  </script>
  
  <style>
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    background-color: transparent;
    border-bottom: 1px solid #e9ecef;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    padding: 20px;
    text-align: center;
    transition: background-color 0.3s ease;
    z-index: 1000;
  }
  
  .header.scrolled {
    background-color: white;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  }
  
  img {
    display: block;
    width: 100%;
    height: auto;
  }
  
  .monogram {
    font-size: 2rem;
    margin-left: 20rem;
    
  }
  
  nav ul {
    gap: 1rem;
    display: flex;
    list-style: none;
    color:black;
    margin-right: 20rem;
  }
  </style>
  