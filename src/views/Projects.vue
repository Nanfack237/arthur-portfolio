<template>
  <section class="projects-section container">
    <h2>My Projects</h2>
    <div class="project-grid">
      <ProjectCard
        title="E-commerce Platform Redesign"
        description="Redesigned and developed a modern e-commerce platform using HTML, CSS, JavaScript, and PHP. Focused on user experience and responsive design. This involved Adobe XD for UI/UX prototyping and Adobe Photoshop for asset creation."
        tools="HTML, CSS, JavaScript, PHP, MySQL, Adobe XD, Adobe Photoshop"
        imageSrc="public/images/ecommerce1.jpeg"
        liveLink="#"
        githubLink="#"
      />
      <ProjectCard
        title="Animated Explainer Video Series"
        description="Produced a series of animated explainer videos for a client's new product launch. Involved scriptwriting, storyboarding, character design, animation, and sound design."
        tools="Adobe Premiere Pro, Adobe After Effects, Illustrator"
        imageSrc="public/images/seriesplanner1.jpeg"
        liveLink="#"
        githubLink="#"
      />
      <ProjectCard
        title="Brand Identity & Marketing Collateral"
        description="Developed a complete brand identity package for a startup, including logo design, color palette, typography, and various marketing materials like brochures and social media graphics. Leveraged Figma for collaborative design."
        tools="Adobe Illustrator, Adobe InDesign, Figma, Canva"
        imageSrc="public/images/marketing1.jpeg"
        liveLink="#"
        githubLink="#"
      />
       <ProjectCard
         title="YouTube Video Management & Monetization"
         description="Managed content, edited videos, handled publication, and optimized for monetization for a YouTube channel. Focused on audience engagement and growth strategies. (From Edmonde Association work)"
         tools="Filmora, YouTube Studio"
         imageSrc="public/images/youtube.jpeg"
         liveLink="https://www.youtube.com/your-channel-link"
         githubLink=""
       />
      </div>
  </section>
</template>

<script setup>
import ProjectCard from '../components/ProjectCard.vue';
</script>

<style scoped>
.projects-section {
  padding: 40px 20px;
}

h2 {
  text-align: center;
  font-size: 2.5em;
  margin-bottom: 40px;
  color: #2c3e50;
}

.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  justify-content: center;
}
</style>