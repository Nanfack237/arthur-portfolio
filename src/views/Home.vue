<template>
  <section class="hero-section">
    <div class="container hero-content">
      <div class="hero-text">
        <h1>GILLES ARTHUR BOKAGNE KEMOGNE</h1>
        <h2>Ingénieur informaticien</h2>
            <p class="tagline">Créateur d'expériences visuelles innovantes où technologie et art se rencontrent.</p>
            <p class="description">Ingénieur passionné par le design, le montage vidéo et l'innovation numérique.</p>
        <router-link to="/projects" class="btn">View My Work</router-link>
        <router-link to="/contact" class="btn secondary-btn">Get in Touch</router-link>
      </div>
      <div class="hero-image">
        <img src="/public/images/profile.jpeg" alt="Gilles Arthur Bokagne Kemogne" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  background-color: #ecf0f1;
  padding: 80px 0 40px; /* Adjust padding-top for fixed navbar */
  text-align: center;
}

.hero-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 40px;
}

@media (min-width: 768px) {
  .hero-content {
    flex-direction: row;
    justify-content: center;
    text-align: left;
  }
  .hero-text {
    flex: 2;
    padding-right: 40px;
  }
  .hero-image {
    flex: 1;
  }
}

.hero-text h1 {
  font-size: 3em;
  margin-bottom: 10px;
  color: #2c3e50;
}

.hero-text h2 {
  font-size: 1.8em;
  color: #3498db;
  margin-bottom: 20px;
}

.hero-text .tagline {
  font-size: 1.2em;
  color: #555;
  margin-bottom: 15px;
}

.hero-text .description {
  font-size: 1.1em;
  color: #777;
  line-height: 1.6;
  margin-bottom: 30px;
}

.hero-image img {
  max-width: 300px;
  border-radius: 50%; /* Circular image */
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}

.btn {
  margin-right: 15px;
  margin-bottom: 15px; /* For mobile stacking */
}

.secondary-btn {
  background-color: #95a5a6;
}

.secondary-btn:hover {
  background-color: #7f8c8d;
}
</style>