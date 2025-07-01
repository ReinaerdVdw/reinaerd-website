<template>
  <section id="projects" class="projects">
    <h3>MY WORK</h3>
    <h2>Featured Projects</h2>
    <p>
      Explore some of my recent Power Platform projects that have helped businesses
      transform their operations.
    </p>

    <div class="projects-grid">
      <ProjectCard
        title="Inventory Management App"
        description="A comprehensive inventory management solution built with Power Apps and integrated with SharePoint."
        tags="Power Apps,Power Automate"
      />

      <ProjectCard
        title="HR Onboarding Portal"
        description="Streamlined employee onboarding process with automated workflows and document management."
        tags="Power Apps,Power Automate"
      />

      <ProjectCard
        title="Customer Support Dashboard"
        description="Real-time customer support analytics dashboard with automated reporting and alerts."
        tags="Power BI,Power Automate"
      />
    </div>

    <div class="view-all">
      <router-link to="/projects" class="btn-outline">View All Projects</router-link>
    </div>
  </section>
</template>

<script setup>
import ProjectCard from './ProjectCard.vue'
</script>

<style scoped>
.projects {
  background: linear-gradient(to bottom, #000 0%, #3b0c5f 50%, #000 100%);
  color: #fff;
  padding: 100px 20px;
  text-align: center;
}

.projects h3 {
  color: #c084fc;
  font-size: 14px;
  letter-spacing: 2px;
  margin-bottom: 10px;
}

.projects h2 {
  font-size: 36px;
  font-weight: bold;
  margin-bottom: 20px;
}

.projects p {
  max-width: 700px;
  margin: 0 auto 60px;
  font-size: 18px;
  line-height: 1.8;
}

.projects-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 30px;
}

.view-all {
  margin-top: 50px;
}

.btn-outline {
  border: 1px solid #c084fc;
  color: #fff;
  padding: 10px 20px;
  border-radius: 5px;
  font-weight: bold;
}
</style>
