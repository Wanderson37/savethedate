<template>
  <q-page-container>
    <q-page>
      <q-carousel v-model="slide" animated infinite swipeable arrows navigation>
        <q-carousel-slide
          v-for="(present, index) in presents"
          :key="index"
          :name="index"
          :img-src="present.image"
        >
          <div class="q-pa-md text-center">
            <q-img :src="present.image" :alt="present.name" class="full-width" />
            <q-card class="q-my-md">
              <q-card-section>
                <div class="text-h6">{{ present.name }}</div>
                <div>{{ present.description }}</div>
                <div class="text-subtitle1 text-bold text-primary q-my-md">
                  {{ present.price }}
                </div>
              </q-card-section>
              <q-card-actions align="center">
                <q-btn label="Comprar" color="primary" @click="buyPresent(present)" />
              </q-card-actions>
            </q-card>
          </div>
        </q-carousel-slide>
      </q-carousel>
    </q-page>
  </q-page-container>
</template>

<script setup>
import { ref } from 'vue'

const slide = ref(0)

const presents = [
  {
    name: 'Panela de Pressão',
    description: 'Panela de pressão inox',
    price: 'R$ 150,00',
    //   image: 'path/to/panela.jpg'
  },
  {
    name: 'Conjunto de Copos',
    description: 'Conjunto com 6 copos',
    price: 'R$ 80,00',
    //   image: 'path/to/copos.jpg'
  },
  // Adicione mais presentes aqui
]

function buyPresent(present) {
  alert(`Você escolheu comprar: ${present.name}`)
}
</script>

<style>
.q-carousel-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding: 1rem;
}

.q-card {
  width: 300px;
}

.full-width {
  width: 100%;
  max-height: 200px;
  object-fit: cover;
}
</style>
