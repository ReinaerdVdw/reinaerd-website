
<template>
  <div class="overlay" @click.self="$emit('close')">
    <div class="modal">
      <h2>{{ project.title }}</h2>
      <div class="tags">
        <span
          v-for="tag in project.tags"
          :key="tag"
          :style="{ backgroundColor: getColor(tag), color: tag === 'Power BI' ? '#000' : '#fff' }"
        >
          {{ tag }}
        </span>
      </div>
      <p>{{ project.longDescription }}</p>

      <button @click="$emit('close')">Close</button>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  project: Object
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
.overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.8);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}

.modal {
  background: #1f1f2e;
  padding: 30px;
  border-radius: 10px;
  max-width: 600px;
  color: #fff;
}

.modal h2 {
  margin-top: 0;
}

.modal button {
  margin-top: 20px;
  background: #c084fc;
  border: none;
  padding: 10px 20px;
  border-radius: 6px;
  color: #fff;
  font-weight: bold;
  cursor: pointer;
}

.tags {
  margin: 10px 0;
}

.tags span {
  display: inline-block;
  padding: 3px 8px;
  font-size: 12px;
  border-radius: 4px;
  margin-right: 5px;
}
</style>
