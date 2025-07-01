<template>
  <section id="intro-block" class="intro-block">
    <div class="container">
      <div class="text">
        <div class="badge">Power Platform Developer</div>
        <h1>Hello, I'm <span>Reinaerd Vandewalle</span></h1>
        <p>
          I create innovative business solutions with Microsoft Power Platform,
          transforming processes through custom applications and automation.
        </p>
        <div class="buttons">
          <a href="#projects" class="btn-primary">View My Work</a>
          <a href="#contact" class="btn-outline">Get In Touch</a>
        </div>
      </div>
      <div class="profile-pic">
        <img
          src="https://reinaerdvandewalle.wordpress.com/wp-content/uploads/2025/06/profpic-1.jpg"
          alt="Profile Picture of Reinaerd Vandewalle"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.intro-block {
  background-color: #000;
  color: #fff;
  padding: 100px 20px;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  gap: 40px;
}

.text {
  flex: 1 1 300px;
  min-width: 280px;
}

.badge {
  display: inline-block;
  background-color: #1f1f1f;
  color: #c084fc;
  padding: 5px 10px;
  border-radius: 15px;
  font-size: 14px;
  margin-bottom: 20px;
}

h1 {
  font-size: 48px;
  font-weight: bold;
  margin: 0 0 20px;
}

h1 span {
  color: #c084fc;
}

p {
  font-size: 18px;
  line-height: 1.6;
  margin-bottom: 40px;
}

.buttons {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.btn-primary {
  background-color: #c084fc;
  color: #fff;
  padding: 10px 20px;
  border-radius: 5px;
  font-weight: bold;
}

.btn-outline {
  border: 2px solid #c084fc;
  color: #fff;
  padding: 10px 20px;
  border-radius: 5px;
  font-weight: bold;
}

.profile-pic {
  flex: 0 0 300px;
  max-width: 300px;
  height: 300px;
  border: 2px solid #c084fc;
  border-radius: 15px;
  overflow: hidden;
}

.profile-pic img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top;
}
</style>
