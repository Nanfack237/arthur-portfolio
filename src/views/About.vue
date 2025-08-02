<template>
  <section class="about-section container">
    <h2>About Me</h2>
    <div class="about-content">
      <div class="about-text">
        <p>Hello! I'm Gilles Arthur Bokagne Kemogne, an IT Engineer deeply passionate about the intersection of technology and creativity. My journey has led me to specialize in visual experiences, blending my skills in software development with a keen eye for design and video production.</p>
        <p>I thrive in dynamic environments where innovation is key, and I'm always eager to learn and adapt to new challenges. My diverse background, from web development to graphic design and video editing, allows me to approach problems with a holistic perspective, delivering impactful and visually appealing solutions.</p>

        <h3>My Strengths</h3>
        <ul class="strengths-list">
          <li>Rigueur</li>
          <li>Proactivité</li>
          <li>Flexibilité</li>
          <li>Travail en équipe</li>
          <li>Adaptabilité</li>
          <li>Organisation</li>
          <li>Analyse</li>
          <li>Créativité</li>
          <li>Curiosité</li>
          <li>Communication</li>
        </ul>

        <h3>Contact Details</h3>
        <p><strong>Email:</strong> <a href="mailto:arthurbokagne@gmail.com">arthurbokagne@gmail.com</a></p>
        <p><strong>Phone:</strong> (+237) 678170085 / 659018606</p>
        <p><strong>Location:</strong> Douala, Bonaberi Rail, Cameroon</p>
        <p><strong>Born:</strong> 29/11/2002</p>
        <p><strong>Nationality:</strong> Cameroonian</p>
        <p><strong>Remote Work:</strong> Not currently seeking remote positions.</p>
      </div>
      <div class="about-sidebar">
        <h3>Languages</h3>
        <ul>
          <li>Français: B2 (Compétence Avancée)</li>
          <li>Anglais: B2 (Compétence Avancée)</li>
        </ul>

        <h3>Interests</h3>
        <ul class="interests-list">
          <li>Football</li>
          <li>Tennis</li>
          <li>Basketball</li>
          <li>GYM</li>
        </ul>

        <h3>Education</h3>
        <div class="education-item">
          <h4>Licence De Technologie En Ingénierie Informatique</h4>
          <p>IUC (Institut Universitaire De Cote), Douala, LT, Cameroon</p>
          <p>September 2022 - July 2023</p>
        </div>
        <div class="education-item">
          <h4>Ingénieur en création vidéo, publie reportage et infographe</h4>
          <p>Chaine de télé "Sun + TV" Bonapriso Hotel Sportif</p>
          <p>Since December 2024</p>
          <p class="details">"J'ai suivi une formation des compétences d'une semaine pour obtenir le poste de créateur de contenu divertissement, que j'ai finalement décroché. J'ai participé à la réalisation de plusieurs émission et j'ai également assuré la diffusion de contenus en tant qu'infographe."</p>
        </div>
        <div class="education-item">
          <h4>Ingénieur Informaticien en Graphique Designeur et Montage Vidéo</h4>
          <p>Precome Engineering Sarr, Douala, LT, Cameroon</p>
          <p>Since August 2023</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  padding: 40px 20px;
}

h2 {
  text-align: center;
  font-size: 2.5em;
  margin-bottom: 40px;
  color: #2c3e50;
}

.about-content {
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
  justify-content: center;
}

.about-text {
  flex: 3;
  min-width: 300px;
  line-height: 1.7;
}

.about-sidebar {
  flex: 1;
  min-width: 250px;
  background-color: #fff;
  padding: 25px;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.about-text h3, .about-sidebar h3 {
  color: #3498db;
  margin-top: 25px;
  margin-bottom: 15px;
  font-size: 1.4em;
}

.about-text ul, .about-sidebar ul {
  list-style: none;
  padding-left: 0;
}

.about-text ul li, .about-sidebar ul li {
  margin-bottom: 8px;
  position: relative;
  padding-left: 20px;
}

.about-text ul li::before, .about-sidebar ul li::before {
  content: "•";
  color: #3498db;
  font-weight: bold;
  display: inline-block;
  width: 1em;
  margin-left: -1em;
}

.education-item {
  margin-bottom: 20px;
  padding-bottom: 15px;
  border-bottom: 1px solid #eee;
}

.education-item:last-child {
  border-bottom: none;
}

.education-item h4 {
  font-size: 1.1em;
  margin-bottom: 5px;
  color: #555;
}

.education-item p {
  font-size: 0.95em;
  color: #777;
  margin-bottom: 3px;
}

.education-item .details {
  font-style: italic;
  font-size: 0.9em;
  color: #666;
  margin-top: 5px;
}

.strengths-list {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 10px;
}

.interests-list {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
}
.interests-list li {
    background-color: #ecf0f1;
    padding: 5px 10px;
    border-radius: 5px;
    font-size: 0.9em;
}
.interests-list li::before {
    display: none;
}
</style>