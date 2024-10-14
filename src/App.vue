<template>
  <div class="app">
    <Header />
    <Hero />
    <About />
    <Products />
    <Services />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import About from './components/About.vue'
import Products from './components/Products.vue'
import Services from './components/Services.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    About,
    Products,
    Services,
    Contact,
    Footer
  }
}
</script>

<style>
.app {
  font-family: 'Roboto', Arial, sans-serif;
  color: #333;
  line-height: 1.6;
}
</style>