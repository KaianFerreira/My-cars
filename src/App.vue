<script setup lang="ts">
import { ref } from 'vue'
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import CarList from './components/CarList.vue'
import Footer from './components/Footer.vue'

const cars = ref([
  {
    id: 1,
    name: 'Tesla Model S',
    price: 79990,
    image: 'https://images.unsplash.com/photo-1555215695-3004980ad54e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&h=400&q=80',
    specs: ['Electric', '396 mi range', '1.99s 0-60 mph']
  },
  {
    id: 2,
    name: 'Porsche 911',
    price: 107550,
    image: 'https://images.unsplash.com/photo-1583121274602-3e2820c69888?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&h=400&q=80',
    specs: ['Gasoline', '443 hp', '3.2s 0-60 mph']
  },
  {
    id: 3,
    name: 'Audi e-tron',
    price: 66995,
    image: 'https://images.unsplash.com/photo-1580273916550-e323be2ae537?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&h=400&q=80',
    specs: ['Electric', '222 mi range', '5.5s 0-60 mph']
  },
  {
    id: 4,
    name: 'BMW i8',
    price: 147500,
    image: 'https://images.unsplash.com/photo-1541899481282-d53bffe3c35d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=600&h=400&q=80',
    specs: ['Hybrid', '369 hp', '4.2s 0-60 mph']
  }
])
</script>

<template>
  <Header />
  <main>
    <Hero />
    <CarList :cars="cars" />
  </main>
  <Footer />
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;
}

#app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

main {
  flex: 1;
  padding: 2rem;
  max-width: 1400px;
  margin: 0 auto;
  width: 100%;
}

@media (max-width: 768px) {
  main {
    padding: 1rem;
  }
}
</style>
