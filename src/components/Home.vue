<template>
  <section id="home" class="home">
    <h1>Welcome to Our Exportation Company</h1>
    <p>Your trusted partner for high-quality agricultural exports</p>
  </section>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<style scoped>
.home {
  background-image: url('https://source.unsplash.com/1600x900/?agriculture');
  background-size: cover;
  background-position: center;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: white;
  padding: 2rem;
}

h1 {
  font-size: 3rem;
  margin-bottom: 1rem;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
}

p {
  font-size: 1.5rem;
  text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
}
</style>