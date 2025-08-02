<template>
  <div id="app-wrapper">
    <Navbar />
    <main class="content-area">
      <router-view />
    </main>
    <Footer />
  </div>
</template>

<script setup>
import Navbar from './components/Navbar.vue';
import Footer from './components/Footer.vue';
</script>

<style>
/* Basic layout styles, enhance with a framework or more detailed CSS */
#app-wrapper {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.content-area {
  flex: 1; /* Allows content to expand and push footer down */
  padding-top: 60px; /* Adjust based on navbar height */
}
</style>