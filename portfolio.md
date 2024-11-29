---
layout: default
title: Portfolio
---

# Portfolio

Welcome to my portfolio! Here, you'll find a showcase of projects that reflect my skills, creativity, and passion for technology. Click on the project cards to explore the details.

---

## Filter Projects
<button class="filter-button" onclick="filterProjects('all')">All</button>
<button class="filter-button" onclick="filterProjects('web')">Web</button>
<button class="filter-button" onclick="filterProjects('mobile')">Mobile</button>
<button class="filter-button" onclick="filterProjects('others')">Others</button>

---

<div class="project-gallery">

### Web Projects

<div class="project-card" data-type="web">
  <img src="/assets/images/project1.jpg" alt="Project 1">
  <h3>Project 1: Personal Portfolio</h3>
  <p>A sleek personal portfolio website built with HTML, CSS, and JavaScript.</p>
  <a href="https://github.com/username/project1" target="_blank">View on GitHub</a>
</div>

<div class="project-card" data-type="web">
  <img src="/assets/images/project2.jpg" alt="Project 2">
  <h3>Project 2: E-commerce Website</h3>
  <p>An e-commerce platform featuring a responsive design and user-friendly interface.</p>
  <a href="https://github.com/username/project2" target="_blank">View on GitHub</a>
</div>

---

### Mobile Projects

<div class="project-card" data-type="mobile">
  <img src="/assets/images/project3.jpg" alt="Project 3">
  <h3>Project 3: Fitness Tracker App</h3>
  <p>A mobile app for tracking workouts and monitoring progress, built with React Native.</p>
  <a href="https://github.com/username/project3" target="_blank">View on GitHub</a>
</div>

<div class="project-card" data-type="mobile">
  <img src="/assets/images/project4.jpg" alt="Project 4">
  <h3>Project 4: Budget Planner</h3>
  <p>An intuitive app to help users plan and track their finances, developed in Flutter.</p>
  <a href="https://github.com/username/project4" target="_blank">View on GitHub</a>
</div>

---

### Other Projects

<div class="project-card" data-type="others">
  <img src="/assets/images/project5.jpg" alt="Project 5">
  <h3>Project 5: Game Prototype</h3>
  <p>A prototype for a strategy board game, designed for both physical and digital formats.</p>
  <a href="https://github.com/username/project5" target="_blank">View on GitHub</a>
</div>

<div class="project-card" data-type="others">
  <img src="/assets/images/project6.jpg" alt="Project 6">
  <h3>Project 6: AI Chatbot</h3>
  <p>An AI-powered chatbot for customer service, implemented using Python and Dialogflow.</p>
  <a href="https://github.com/username/project6" target="_blank">View on GitHub</a>
</div>

</div>

---

<script>
function filterProjects(type) {
  const cards = document.querySelectorAll('.project-card');
  cards.forEach(card => {
    card.style.display = (type === 'all' || card.dataset.type === type) ? 'block' : 'none';
  });
}
</script>
