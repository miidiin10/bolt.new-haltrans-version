<template>
  <footer class="footer">
    <div class="container">
      <p>&copy; {{ currentYear }} Haltrans Commodities. All rights reserved.</p>
      <div class="social-links">
        <a href="#" target="_blank" rel="noopener noreferrer">Facebook</a>
        <a href="#" target="_blank" rel="noopener noreferrer">Twitter</a>
        <a href="#" target="_blank" rel="noopener noreferrer">LinkedIn</a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  computed: {
    currentYear() {
      return new Date().getFullYear()
    }
  }
}
</script>

<style scoped>
.footer {
  background-color: #333;
  color: white;
  padding: 2rem 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.social-links a {
  color: white;
  text-decoration: none;
  margin-left: 1rem;
}

.social-links a:hover {
  text-decoration: underline;
}
</style>