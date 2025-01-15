<template>
  <div class="container">
    <img class="img-couple" src="/couple.jpg" alt="image of couple" />
    <div class="name-div">
      <span class="name-couple"> Carolina e Wanderson </span>
      <span class="event-date">24.06.2025</span>
    </div>
  </div>
</template>
<style>
img {
  padding: 0;
  width: 100%;
  height: 100%;
  left: 0;
  width: 100%;
  height: 100vh;
  object-fit: cover;
  z-index: -1;
}
.container {
  position: relative;
  width: 100%;
  margin: 0 auto;
  text-align: center;
}
.name-couple {
  display: block;
  font-size: 5rem;
  color: white;
  top: 50vh;
  left: 50%;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}
.name-div {
  position: absolute;
  top: 70vh;
  left: 50%;
  transform: translate(-50%, -50%);
}
.event-date {
  display: block;
  font-size: 3rem;
  color: white;
  top: 60vh;
  left: 50%;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}
</style>
