<template>
  <div class="card">
    <div class="image-placeholder">
      <span>Image</span>
    </div>
    <div class="content">
      <div class="tags">
        <span
          v-for="tag in tagsArray"
          :key="tag"
          :style="{ backgroundColor: getColor(tag), color: tag === 'Power BI' ? '#000' : '#fff' }"
        >
          {{ tag }}
        </span>
      </div>
      <h4>{{ title }}</h4>
      <p>{{ description }}</p>
      <a href="#">Learn more →</a>
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  title: String,
  description: String,
  tags: String,
})

const tagsArray = computed(() => props.tags.split(','))

function getColor(tag) {
  switch (tag) {
    case 'Power Apps':
      return '#7c3aed'
    case 'Power Automate':
      return '#2563eb'
    case 'Power BI':
      return '#facc15'
    default:
      return '#999'
  }
}
</script>

<style scoped>
.card {
  background-color: #1f2a3a;
  width: 320px;
  border-radius: 10px;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.3);
}

.image-placeholder {
  height: 180px;
  background-color: #d1d5db;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #999;
}

.content {
  padding: 20px;
  text-align: left;
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

h4 {
  margin: 0 0 10px;
  font-size: 18px;
}

p {
  font-size: 14px;
  line-height: 1.6;
}

a {
  display: inline-block;
  margin-top: 10px;
  color: #c084fc;
  font-weight: bold;
  font-size: 14px;
  text-decoration: none;
}
</style>
