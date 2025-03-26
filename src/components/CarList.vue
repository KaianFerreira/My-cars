<script setup lang="ts">
import { defineProps } from 'vue'

defineProps({
  cars: {
    type: Array,
    required: true
  }
})
</script>

<template>
  <section class="car-list">
    <h2 class="section-title">Featured Vehicles</h2>
    <div class="cars-grid">
      <div v-for="car in cars" :key="car.id" class="car-card">
        <img :src="car.image" :alt="car.name" class="car-image" />
        <div class="car-details">
          <h3>{{ car.name }}</h3>
          <ul class="specs">
            <li v-for="(spec, index) in car.specs" :key="index">{{ spec }}</li>
          </ul>
          <div class="price">${{ car.price.toLocaleString() }}</div>
          <button class="view-button">View Details</button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section-title {
  text-align: center;
  margin-bottom: 3rem;
  font-size: 2.5rem;
  color: #111827;
  font-weight: 700;
}

.cars-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
  gap: 2rem;
  padding: 0 2rem;
}

.car-card {
  background: white;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s, box-shadow 0.3s;
  border: 1px solid #e5e7eb;
}

.car-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1);
}

.car-image {
  width: 100%;
  height: 220px;
  object-fit: cover;
}

.car-details {
  padding: 1.5rem;
  text-align: left;
}

.car-details h3 {
  margin-bottom: 1rem;
  font-size: 1.4rem;
  color: #111827;
}

.specs {
  list-style: none;
  margin-bottom: 1.5rem;
  color: #4b5563;
  padding-left: 0;
}

.specs li {
  margin-bottom: 0.5rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.specs li::before {
  content: '•';
  color: #2563eb;
}

.price {
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 1.5rem;
  color: #111827;
}

.view-button {
  width: 100%;
  padding: 0.8rem;
  background-color: #111827;
  color: white;
  border: none;
  border-radius: 8px;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.2s;
}

.view-button:hover {
  background-color: #1e293b;
}

@media (max-width: 768px) {
  .cars-grid {
    grid-template-columns: 1fr;
    padding: 0 1rem;
  }
}
</style>
