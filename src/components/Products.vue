<template>
  <section id="products" class="products">
    <div class="container">
      <h2>Our Products</h2>
      <div class="product-grid">
        <div v-for="product in products" :key="product.name" class="product-card">
          <img :src="product.image" :alt="product.name">
          <h3>{{ product.name }}</h3>
          <p>{{ product.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Products',
  data() {
    return {
      products: [
        {
          name: 'Dry Split Ginger',
          description: 'High-quality dried ginger, perfect for culinary and medicinal uses.',
          image: 'https://haltrans-commodities.b12sites.com/images/ginger.jpg'
        },
        {
          name: 'Dry Hibiscus Sifting',
          description: 'Premium dried hibiscus flowers, ideal for teas and natural food coloring.',
          image: 'https://haltrans-commodities.b12sites.com/images/hibiscus.jpg'
        },
        {
          name: 'Cassia Tora',
          description: 'Versatile legume seeds used in various industries including food and cosmetics.',
          image: 'https://haltrans-commodities.b12sites.com/images/cassia-tora.jpg'
        },
        {
          name: 'Soya Beans',
          description: 'Nutrient-rich soya beans, perfect for food production and animal feed.',
          image: 'https://haltrans-commodities.b12sites.com/images/soya-beans.jpg'
        }
      ]
    }
  }
}
</script>

<style scoped>
.products {
  padding: 4rem 2rem;
  background-color: #ffffff;
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

.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.product-card {
  background-color: #f8f9fa;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.product-card:hover {
  transform: translateY(-5px);
}

.product-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.product-card h3 {
  padding: 1rem;
  margin: 0;
  color: #333;
}

.product-card p {
  padding: 0 1rem 1rem;
  color: #666;
}
</style>