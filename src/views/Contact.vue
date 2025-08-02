<template>
  <section class="contact-section container">
    <h2>Get in Touch</h2>
    <div class="contact-content">
      <div class="contact-info">
        <h3>Contact Details</h3>
        <p><i class="icon fas fa-envelope"></i> Email: <a href="mailto:arthurbokagne@gmail.com">arthurbokagne@gmail.com</a></p>
        <p><i class="icon fas fa-phone"></i> Phone: (+237) 678170085 / 659018606</p>
        <p><i class="icon fas fa-map-marker-alt"></i> Location: Douala, Bonaberi Rail, Cameroon</p>
        <p>Feel free to reach out to discuss potential projects, collaborations, or just to say hello!</p>
      </div>
      <div class="contact-form-wrapper">
        <h3>Send Me a Message</h3>
        <form @submit.prevent="submitForm" class="contact-form">
          <div class="form-group">
            <label for="name">Name:</label>
            <input type="text" id="name" v-model="form.name" required />
          </div>
          <div class="form-group">
            <label for="email">Email:</label>
            <input type="email" id="email" v-model="form.email" required />
          </div>
          <div class="form-group">
            <label for="message">Message:</label>
            <textarea id="message" v-model="form.message" rows="5" required></textarea>
          </div>
          <button type="submit" class="btn">Send Message</button>
        </form>
        <p v-if="messageSent" class="success-message">Message sent successfully!</p>
        <p v-if="errorMessage" class="error-message">{{ errorMessage }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

const form = ref({
  name: '',
  email: '',
  message: '',
});

const messageSent = ref(false);
const errorMessage = ref('');

const submitForm = () => {
  // In a real application, you would send this data to a backend API
  // or a service like Formspree, Netlify Forms, etc.
  console.log('Form submitted:', form.value);

  // Simulate API call
  setTimeout(() => {
    if (Math.random() > 0.1) { // 90% chance of success
      messageSent.value = true;
      errorMessage.value = '';
      form.value = { name: '', email: '', message: '' }; // Clear form
    } else {
      errorMessage.value = 'Failed to send message. Please try again later.';
      messageSent.value = false;
    }
  }, 1000);
};
</script>

<style scoped>
.contact-section {
  padding: 40px 20px;
}

h2 {
  text-align: center;
  font-size: 2.5em;
  margin-bottom: 40px;
  color: #2c3e50;
}

.contact-content {
  display: flex;
  flex-wrap: wrap;
  gap: 50px;
  justify-content: center;
}

.contact-info, .contact-form-wrapper {
  flex: 1;
  min-width: 300px;
  background-color: white;
  padding: 30px;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.contact-info h3, .contact-form-wrapper h3 {
  color: #3498db;
  margin-top: 0;
  margin-bottom: 20px;
  font-size: 1.5em;
}

.contact-info p {
  margin-bottom: 15px;
  font-size: 1.1em;
  color: #555;
}

.contact-info p a {
  color: #3498db;
}

.contact-info .icon {
  margin-right: 10px;
  color: #2c3e50;
}

.contact-form .form-group {
  margin-bottom: 20px;
}

.contact-form label {
  display: block;
  margin-bottom: 8px;
  font-weight: bold;
  color: #333;
}

.contact-form input[type="text"],
.contact-form input[type="email"],
.contact-form textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #ddd;
  border-radius: 5px;
  font-size: 1em;
  box-sizing: border-box; /* Include padding in width */
}

.contact-form textarea {
  resize: vertical;
}

.contact-form .btn {
  width: auto;
  padding: 12px 25px;
  font-size: 1.1em;
  cursor: pointer;
}

.success-message {
  color: green;
  margin-top: 15px;
  text-align: center;
}

.error-message {
  color: red;
  margin-top: 15px;
  text-align: center;
}
</style>