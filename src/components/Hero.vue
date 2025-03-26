<script setup lang="ts"></script>

<template>
  <section class="hero">
    <div class="hero-content">
      <h2>Premium Luxury Cars</h2>
      <p>Discover the finest selection of high-performance vehicles</p>
      <button class="hero-button">Browse Inventory</button>
    </div>
  </section>
</template>

<style scoped>
.hero {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url('https://images.unsplash.com/photo-1494972308805-463bc619d34e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1600&h=900&q=80');
  background-size: cover;
  background-position: center;
  height: 70vh;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  text-align: center;
  margin-bottom: 3rem;
}

.hero-content {
  max-width: 800px;
  padding: 2rem;
}

.hero h2 {
  font-size: 3.5rem;
  margin-bottom: 1.5rem;
  font-weight: 800;
  line-height: 1.2;
}

.hero p {
  font-size: 1.25rem;
  margin-bottom: 2.5rem;
  opacity: 0.9;
}

.hero-button {
  background-color: transparent;
  color: white;
  border: 2px solid white;
  padding: 0.8rem 2.5rem;
  font-size: 1rem;
  font-weight: 600;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s;
}

.hero-button:hover {
  background-color: white;
  color: #111827;
}

@media (max-width: 768px) {
  .hero {
    height: 60vh;
  }

  .hero h2 {
    font-size: 2.5rem;
  }

  .hero p {
    font-size: 1.1rem;
  }
}
</style>
