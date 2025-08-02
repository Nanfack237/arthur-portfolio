<template>
  <section class="experience-section container">
    <h2>Professional Experience</h2>
    <div class="timeline">
      <ExperienceItem
        title="Web Designer Et Web Développeur"
        company="SUN+TV Bonapriso Hotel Sportif"
        duration="Since December 2024"
        location="Douala"
        :tasks="[
          'Adobe XD',
          'Adobe Photoshop',
          'Editeur de code',
          'Language De Programmation (HTML/CSS, JavaScript, PHP, Python)',
          'Base De Données (MySQL)',
          'Outils de test et de déblogage (Cypress, Jest)'
        ]"
        side="left"
      />
      <ExperienceItem
        title="Infographe Et Créateur de Vidéo"
        company="SUN +TV Bonapriso Hotel Sportif"
        duration="Since December 2024"
        location="Douala"
        :tasks="[
          'Adobe Creative Cloud (Adobe Photoshop, Adobe Illustrator, Adobe InDesign)',
          'Graphisme et Illustration (Figma, Canva et Sketch)',
          'Edition Vidéo (Adobe Premiere Pro, DaVinci Resolve, Filmora)',
          'Animation et Motion Design (Adobe After Effects)',
          'Conception de données et Visualisation (Tableau)',
          'Participated in the realization of several shows.',
          'Ensured content dissemination as an infographer.'
        ]"
        side="right"
      />
      <ExperienceItem
        title="Enseignant En Programmation et Graphique Designer"
        company="Precome Engineering Sarr"
        duration="July 2023 to November 2024"
        location="Douala, LT, Cameroon"
        :tasks="[
          'Formation en HTML, CSS, PHP',
          'Photoshop',
          'Canva',
          'Gimp',
          'Filmora',
          'Microsoft Word, Excel, PowerPoint'
        ]"
        side="left"
      />
      <ExperienceItem
        title="Administrator des Montage Videos"
        company="Edmonde Association"
        duration="June 2021 to October 2021"
        location="Douala, LT, Cameroon"
        :tasks="[
          'Montage des video',
          'Gerer les Videos Crée',
          'Publication des Videos Sur Youtube',
          'Gestion des revenues'
        ]"
        side="right"
      />
      <ExperienceItem
        title="Stagiaire En Camrail"
        company="Camrail Cameroun"
        duration="May 2020 to August 2020"
        location="Douala, LT, Cameroon"
        :tasks="[
          'Migration Des Machines',
          'Gestionnaire Des Pannes Techniques',
          'Installation Des Logiciels',
          'Gestionnaire Des Cable Réseaux',
          'Assistant du Chef du Departement Informatique'
        ]"
        side="left"
      />
    </div>
  </section>
</template>

<script setup>
import ExperienceItem from '../components/ExperienceItem.vue';
</script>

<style scoped>
.experience-section {
  padding: 40px 20px;
}

h2 {
  text-align: center;
  font-size: 2.5em;
  margin-bottom: 40px;
  color: #2c3e50;
}

.timeline {
  position: relative;
  max-width: 900px;
  margin: 0 auto;
  padding: 20px 0;
}

.timeline::after {
  content: '';
  position: absolute;
  width: 4px;
  background-color: #3498db;
  top: 0;
  bottom: 0;
  left: 50%;
  margin-left: -2px;
}

/* On smaller screens, the timeline will be on the left */
@media screen and (max-width: 768px) {
  .timeline::after {
    left: 20px;
  }
}
</style>