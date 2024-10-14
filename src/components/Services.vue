<template>
  <section id="services" class="services">
    <div class="container">
      <h2>Our Services</h2>
      <div class="service-grid">
        <div class="service-card" v-for="service in services" :key="service.title">
          <h3>{{ service.title }}</h3>
          <p>{{ service.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Services',
  data() {
    return {
      services: [
        {
          title: 'Agricultural Commodities Trading',
          description: 'We source and supply high-quality agricultural commodities to meet global demand.'
        },
        {
          title: 'Quality Assurance',
          description: 'Our rigorous quality control ensures that all products meet international standards.'
        },
        {
          title: 'Logistics and Transportation',
          description: 'We provide efficient logistics solutions to ensure timely delivery of goods.'
        },
        {
          title: 'Market Analysis and Consulting',
          description: 'Our experts offer valuable insights and advice on market trends and opportunities.'
        }
      ]
    }
  }
}
</script>

<style scoped>
.services {
  padding: 4rem 2rem;
  background-color: #f8f9fa;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

h2 {
  color: #007bff;
  margin-bottom: 2rem;
  text-align: center;
}

.service-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.service-card {
  background-color: #ffffff;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.service-card h3 {
  color: #007bff;
  margin-bottom: 1rem;
}

.service-card p {
  color: #666;
}
</style>