
<template>
  <section class="projects-view">
    <h2>All Projects</h2>

    <div class="projects-list">
      <ProjectDetailCard
        v-for="(project, index) in projects"
        :key="project.id"
        :project="project"
        :reverse="index % 2 === 1"
        @open="openModal"
      />
    </div>

    <ProjectModal
      v-if="modalProject"
      :project="modalProject"
      @close="modalProject = null"
    />
  </section>
</template>

<script setup>
import { ref } from 'vue'
import ProjectDetailCard from '../components/ProjectDetailCard.vue'
import ProjectModal from '../components/ProjectModal.vue'

const modalProject = ref(null)

function openModal(project) {
  modalProject.value = project
}

const projects = ref([
  {
    id: 1,
    title: 'Inventory Management App',
    description: 'A comprehensive inventory management solution built with Power Apps and integrated with SharePoint.',
    longDescription: 'This app provides complete tracking, barcode scanning, reporting, and user role management for enterprise-level inventory needs.',
    tags: ['Power Apps', 'Power Automate'],
    images: [
      'https://via.placeholder.com/500x300?text=Inventory+1',
      'https://via.placeholder.com/500x300?text=Inventory+2',
      'https://via.placeholder.com/500x300?text=Inventory+3'
    ]
  },
  {
    id: 2,
    title: 'HR Onboarding Portal',
    description: 'Streamlined employee onboarding process with automated workflows and document management.',
    longDescription: 'The portal enables HR teams to manage new hire tasks, documents, and training programs, integrated with Power Automate for automated communications.',
    tags: ['Power Apps', 'Power Automate'],
    images: [
      'https://via.placeholder.com/500x300?text=HR+Portal+1',
      'https://via.placeholder.com/500x300?text=HR+Portal+2',
      'https://via.placeholder.com/500x300?text=HR+Portal+3'
    ]
  },
  {
    id: 3,
    title: 'Customer Support Dashboard',
    description: 'Real-time customer support analytics dashboard with automated reporting and alerts.',
    longDescription: 'This Power BI dashboard integrates ticketing data, tracks SLA metrics, and triggers proactive notifications for critical issues.',
    tags: ['Power BI', 'Power Automate'],
    images: [
      'https://via.placeholder.com/500x300?text=Support+1',
      'https://via.placeholder.com/500x300?text=Support+2',
      'https://via.placeholder.com/500x300?text=Support+3'
    ]
  }
])
</script>

<style scoped>
.projects-view {
  padding: 60px 20px;
  max-width: 1200px;
  margin: 0 auto;
}

.projects-list {
  display: flex;
  flex-direction: column;
  gap: 60px;
}

.projects-view h2 {
  color: #c084fc;
  text-align: center;
  font-size: 36px;
  margin-bottom: 40px;
}
</style>
