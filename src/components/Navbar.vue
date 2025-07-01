<template>
  <div class="navbar">
    <div class="logo">RV</div>
    <div class="nav-links">
      <ul>
  <li><router-link to="/#about-me">About</router-link></li>
  <li><router-link to="/#skills">Skills</router-link></li>
  <li><router-link to="/#projects">Projects</router-link></li>
  <li><router-link to="/#contact">Contact</router-link></li>
</ul>

      <a href="#" class="resume-btn">Resume</a>
    </div>
  </div>
</template>

<script setup>
import { RouterLink } from 'vue-router'
</script>


<style scoped>
.navbar {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  padding: 20px;
}

.logo {
  font-size: 20px;
  font-weight: bold;
  color: #c084fc;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 30px;
  flex-wrap: wrap;
}

.nav-links ul {
  display: flex;
  gap: 30px;
  list-style: none;
  margin: 0;
  padding: 0;
}

.nav-links a {
  color: #fff;
  font-size: 16px;
}

.resume-btn {
  background-color: #c084fc;
  color: #fff;
  padding: 8px 16px;
  border-radius: 6px;
  font-weight: bold;
  font-size: 16px;
}
</style>
