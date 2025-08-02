<template>
  <nav class="navbar">
    <div class="container navbar-content">
      <router-link to="/" class="site-logo">Gilles B.</router-link>
      <ul class="nav-links">
        <li><router-link to="/about">About Me</router-link></li>
        <li><router-link to="/experience">Experience</router-link></li>
        <li><router-link to="/projects">Projects</router-link></li>
        <li><router-link to="/contact">Contact</router-link></li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  background-color: #2c3e50;
  color: white;
  padding: 15px 0;
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 1000;
  box-shadow: 0 2px 5px rgba(0,0,0,0.2);
}

.navbar-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.site-logo {
  color: white;
  font-size: 1.5em;
  font-weight: bold;
}

.nav-links {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
}

.nav-links li {
  margin-left: 20px;
}

.nav-links a {
  color: white;
  font-weight: bold;
  transition: color 0.3s ease;
}

.nav-links a:hover,
.nav-links a.router-link-active {
  color: #3498db;
  text-decoration: none;
}
</style>