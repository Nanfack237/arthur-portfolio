<template>
  <div class="project-card">
    <div class="project-image-wrapper">
      <img :src="imageSrc" :alt="title" class="project-image" />
    </div>
    <div class="project-details">
      <h3>{{ title }}</h3>
      <p class="project-description">{{ description }}</p>
      <p class="project-tools"><strong>Tools:</strong> {{ tools }}</p>
      <!-- <div class="project-links">
        <a v-if="liveLink" :href="liveLink" target="_blank" rel="noopener noreferrer" class="btn small-btn">View Live</a>
      </div> -->
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  title: String,
  description: String,
  tools: String,
  imageSrc: String,
  liveLink: String,
  githubLink: String,
});
</script>

<style scoped>
.project-card {
  background-color: white;
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  overflow: hidden;
  display: flex;
  flex-direction: column;
  transition: transform 0.3s ease;
}

.project-card:hover {
  transform: translateY(-5px);
}

.project-image-wrapper {
  width: 100%;
  height: 200px; /* Fixed height for consistency */
  overflow: hidden;
}

.project-image {
  width: 100%;
  height: 100%;
  object-fit: cover; /* Ensures image covers the area without distortion */
  display: block;
}

.project-details {
  padding: 20px;
  flex-grow: 1; /* Allows details section to take remaining height */
  display: flex;
  flex-direction: column;
}

.project-details h3 {
  font-size: 1.5em;
  margin-top: 0;
  margin-bottom: 10px;
  color: #2c3e50;
}

.project-description {
  font-size: 0.95em;
  color: #555;
  line-height: 1.6;
  margin-bottom: 15px;
  flex-grow: 1; /* Pushes links to the bottom */
}

.project-tools {
  font-size: 0.85em;
  color: #777;
  margin-bottom: 20px;
}

.project-links {
  margin-top: auto; /* Pushes links to the bottom */
  display: flex;
  gap: 10px;
}

.small-btn {
  padding: 8px 15px;
  font-size: 0.9em;
}

.github-btn {
  background-color: #333; /* Darker color for GitHub */
}

.github-btn:hover {
  background-color: #555;
}
</style>