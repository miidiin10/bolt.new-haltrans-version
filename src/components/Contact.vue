<template>
  <section id="contact" class="contact">
    <div class="container">
      <h2>Contact Us</h2>
      <form @submit.prevent="submitForm">
        <div class="form-group">
          <label for="name">Name</label>
          <input v-model="name" type="text" id="name" required>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input v-model="email" type="email" id="email" required>
        </div>
        <div class="form-group">
          <label for="message">Message</label>
          <textarea v-model="message" id="message" required></textarea>
        </div>
        <button type="submit">Send Message</button>
      </form>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      name: '',
      email: '',
      message: ''
    }
  },
  methods: {
    submitForm() {
      console.log('Form submitted:', { name: this.name, email: this.email, message: this.message })
      // Reset form fields
      this.name = ''
      this.email = ''
      this.message = ''
      // Here you would typically send the form data to a server
    }
  }
}
</script>

<style scoped>
.contact {
  padding: 4rem 2rem;
  background-color: #ffffff;
}

.container {
  max-width: 600px;
  margin: 0 auto;
}

h2 {
  color: #007bff;
  margin-bottom: 2rem;
  text-align: center;
}

.form-group {
  margin-bottom: 1.5rem;
}

label {
  display: block;
  margin-bottom: 0.5rem;
  color: #333;
}

input, textarea {
  width: 100%;
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 4px;
}

textarea {
  height: 150px;
}

button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  cursor: pointer;
  border-radius: 4px;
  transition: background-color 0.3s ease;
}

button:hover {
  background-color: #0056b3;
}
</style>