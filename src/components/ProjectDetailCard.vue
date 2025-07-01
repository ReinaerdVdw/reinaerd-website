
<template>
  <div
    class="project-detail"
    :class="{ reverse }"
  >
    <div class="text-content">
      <div class="tags">
        <span
          v-for="tag in project.tags"
          :key="tag"
          :style="{ backgroundColor: getColor(tag), color: tag === 'Power BI' ? '#000' : '#fff' }"
        >
          {{ tag }}
        </span>
      </div>
      <h3>{{ project.title }}</h3>
      <p>{{ project.description }}</p>
      <button @click="$emit('open', project)">View Project</button>
    </div>

    <div class="carousel-wrapper">
      <Carousel :itemsToShow="1" autoplay>
        <Slide
          v-for="(img, idx) in project.images"
          :key="idx"
        >
          <img :src="img" alt="project image" />
        </Slide>
      </Carousel>
    </div>
  </div>
</template>

<script setup>
import { Carousel, Slide } from 'vue3-carousel'

const props = defineProps({
  project: Object,
  reverse: Boolean
})

function getColor(tag) {
  switch (tag) {
    case 'Power Apps': return '#7c3aed'
    case 'Power Automate': return '#2563eb'
    case 'Power BI': return '#facc15'
    default: return '#999'
  }
}
</script>

<style scoped>
.project-detail {
  display: flex;
  gap: 40px;
  align-items: center;
  background-color: #1f2a3a;   /* 👈 add this */
  border-radius: 10px;
  padding: 30px;
}


.project-detail.reverse {
  flex-direction: row-reverse;
}

.text-content {
  flex: 1;
}

.text-content h3 {
  font-size: 28px;
  color: #fff;
}

.text-content p {
  color: #ccc;
  margin: 15px 0;
}

.text-content button {
  background: #c084fc;
  color: #fff;
  border: none;
  padding: 10px 20px;
  border-radius: 6px;
  font-weight: bold;
  cursor: pointer;
}

.tags {
  margin-bottom: 10px;
}

.tags span {
  display: inline-block;
  padding: 3px 8px;
  font-size: 12px;
  border-radius: 4px;
  margin-right: 5px;
  margin-bottom: 5px;
}

.carousel-wrapper {
  flex: 1;
  max-width: 600px;
}

.carousel-wrapper img {
  width: 100%;
  border-radius: 10px;
}
</style>
