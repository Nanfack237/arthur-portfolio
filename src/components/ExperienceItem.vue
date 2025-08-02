<template>
  <div class="timeline-item">
    <div class="timeline-content">
      <h3>{{ title }}</h3>
      <h4>{{ company }} <span v-if="location"> - {{ location }}</span></h4>
      <p class="duration">{{ duration }}</p>
      <ul>
        <li v-for="(task, index) in tasks" :key="index">{{ task }}</li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  title: String,
  company: String,
  duration: String,
  location: String,
  tasks: Array,
});
</script>

<style scoped>
.timeline-item {
  padding: 10px 0;
  position: relative;
  width: 50%;
  padding-left: 30px; /* Space for the dot */
  margin-bottom: 20px;
  box-sizing: border-box;
}

/* Left side of timeline */
.timeline-item:nth-child(odd) {
  left: 0;
}

/* Right side of timeline */
.timeline-item:nth-child(even) {
  left: 50%;
  padding-left: 0;
  padding-right: 30px; /* Space for the dot */
}

/* Dot on the timeline */
.timeline-item::after {
  content: '';
  position: absolute;
  width: 16px;
  height: 16px;
  background-color: #3498db;
  border-radius: 50%;
  z-index: 1;
  top: 20px;
  /* Adjust position based on left/right */
  right: -8px; /* For odd (left) items */
}

.timeline-item:nth-child(even)::after {
  left: -8px; /* For even (right) items */
}

.timeline-content {
  background-color: white;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.timeline-content h3 {
  color: #2c3e50;
  margin-top: 0;
  margin-bottom: 5px;
  font-size: 1.2em;
}

.timeline-content h4 {
  color: #3498db;
  margin-bottom: 10px;
  font-size: 1em;
}

.timeline-content .duration {
  font-style: italic;
  color: #777;
  margin-bottom: 15px;
  font-size: 0.9em;
}

.timeline-content ul {
  list-style: disc;
  padding-left: 20px;
  margin: 0;
}

.timeline-content ul li {
  margin-bottom: 5px;
  font-size: 0.95em;
  color: #555;
}

/* Media query for smaller screens */
@media screen and (max-width: 768px) {
  .timeline-item {
    width: 100%;
    padding-left: 50px; /* More space for the left-aligned dot */
    padding-right: 15px; /* Ensure some right padding */
    left: 0 !important; /* Force all items to left */
  }

  .timeline-item::after {
    left: 12px !important; /* Adjust dot position for left-aligned */
    right: auto; /* Remove right position */
  }

  .timeline-item:nth-child(even)::after {
    left: 12px !important; /* Ensure consistency */
  }
}
</style>