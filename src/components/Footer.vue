<template>
  <footer class="footer">
    <div class="container">
      <p>&copy; {{ currentYear }} Gilles Arthur Bokagne Kemogne. All rights reserved.</p>
    
    </div>
  </footer>
</template>

<script setup>
import { ref } from 'vue';

const currentYear = ref(new Date().getFullYear());
</script>

<style scoped>
.footer {
  background-color: #2c3e50;
  color: white;
  padding: 20px 0;
  text-align: center;
  margin-top: 40px;
}

.footer p {
  margin: 5px 0;
  font-size: 0.9em;
}
</style>