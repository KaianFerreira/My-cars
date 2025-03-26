<script setup lang="ts">
const navItems = [
  { name: 'Home', link: '#' },
  { name: 'Inventory', link: '#' },
  { name: 'About', link: '#' },
  { name: 'Contact', link: '#' }
]
</script>

<template>
  <header class="header">
    <div class="container">
      <h1 class="logo">LUXCARS</h1>
      <nav class="nav">
        <ul>
          <li v-for="item in navItems" :key="item.name">
            <a :href="item.link">{{ item.name }}</a>
          </li>
        </ul>
      </nav>
      <button class="cta-button">Sign In</button>
    </div>
  </header>
</template>

<style scoped>
.header {
  background-color: #ffffff;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 100;
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  max-width: 1400px;
  margin: 0 auto;
}

.logo {
  font-weight: 800;
  font-size: 1.5rem;
  color: #111827;
  letter-spacing: -0.5px;
}

.nav ul {
  display: flex;
  gap: 2rem;
  list-style: none;
}

.nav a {
  color: #4b5563;
  font-weight: 500;
  transition: color 0.2s;
  padding: 0.5rem 0;
  position: relative;
}

.nav a:hover {
  color: #111827;
}

.nav a::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background-color: #2563eb;
  transition: width 0.2s;
}

.nav a:hover::after {
  width: 100%;
}

.cta-button {
  background-color: #111827;
  color: white;
  border: none;
  padding: 0.6rem 1.5rem;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.2s;
}

.cta-button:hover {
  background-color: #1e293b;
}

@media (max-width: 768px) {
  .container {
    flex-direction: column;
    gap: 1rem;
    padding: 1rem;
  }

  .nav ul {
    gap: 1rem;
  }
}
</style>
