<script setup lang="ts"></script>

<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-section">
        <h3>LUXCARS</h3>
        <p>Premium luxury vehicles for the discerning driver.</p>
      </div>
      <div class="footer-section">
        <h4>Quick Links</h4>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">Inventory</a></li>
          <li><a href="#">About Us</a></li>
          <li><a href="#">Contact</a></li>
        </ul>
      </div>
      <div class="footer-section">
        <h4>Contact</h4>
        <p>123 Luxury Avenue</p>
        <p>Beverly Hills, CA 90210</p>
        <p>info@luxcars.com</p>
      </div>
    </div>
    <div class="footer-bottom">
      <p>&copy; 2023 LUXCARS. All rights reserved.</p>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #333;
  color: white;
  padding: 2rem 0 0;
  margin-top: 3rem;
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;
}

.footer-section {
  margin-bottom: 2rem;
}

.footer-section h3 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.footer-section h4 {
  font-size: 1.2rem;
  margin-bottom: 1rem;
}

.footer-section ul {
  list-style: none;
}

.footer-section ul li {
  margin-bottom: 0.5rem;
}

.footer-section a {
  color: #ccc;
  text-decoration: none;
  transition: color 0.3s;
}

.footer-section a:hover {
  color: white;
}

.footer-bottom {
  text-align: center;
  padding: 1rem;
  border-top: 1px solid #444;
  margin-top: 2rem;
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
    padding: 0 1rem;
  }
}
</style>
