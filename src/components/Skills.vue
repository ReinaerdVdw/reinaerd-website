<template>
  <section id="skills" class="skills">
    <h3>MY SKILLS</h3>
    <h2>Power Platform Expertise</h2>
    <p>
      I specialize in Microsoft Power Platform technologies, creating custom business
      solutions that drive efficiency and innovation.
    </p>

    <div class="skills-grid">
      <!-- Power Apps -->
      <div class="skill-card">
        <div class="icon" style="background-color: #7c3aed;">
          🟪
        </div>
        <h3>Power Apps</h3>
        <p>Creating custom business applications with both canvas and model-driven apps, focusing on user experience and business value.</p>
        <div class="tags">
          <span style="background-color: #7c3aed;">Canvas Apps</span>
          <span style="background-color: #7c3aed;">Model-driven Apps</span>
          <span style="background-color: #7c3aed;">Portals</span>
        </div>
      </div>

      <!-- Power Automate -->
      <div class="skill-card">
        <div class="icon" style="background-color: #2563eb;">
          🔁
        </div>
        <h3>Power Automate</h3>
        <p>Building automated workflows that connect apps and services, reducing manual tasks and improving business processes.</p>
        <div class="tags">
          <span style="background-color: #2563eb;">Cloud Flows</span>
          <span style="background-color: #2563eb;">Business Process Flows</span>
          <span style="background-color: #2563eb;">UI Flows</span>
        </div>
      </div>

      <!-- Power BI -->
      <div class="skill-card">
        <div class="icon" style="background-color: #facc15; color: #000;">
          📊
        </div>
        <h3>Power BI</h3>
        <p>Creating interactive data visualizations and business intelligence dashboards that provide actionable insights.</p>
        <div class="tags">
          <span style="background-color: #facc15; color: #000;">Reports</span>
          <span style="background-color: #facc15; color: #000;">Dashboards</span>
          <span style="background-color: #facc15; color: #000;">Data Modeling</span>
        </div>
      </div>

      <!-- Power Pages -->
      <div class="skill-card">
        <div class="icon" style="background-color: #3b82f6;">
          🌐
        </div>
        <h3>Power Pages</h3>
        <p>Designing secure, low-code external-facing websites that extend business processes to partners, vendors, and customers.</p>
        <div class="tags">
          <span style="background-color: #3b82f6;">Web Portals</span>
          <span style="background-color: #3b82f6;">External Access</span>
          <span style="background-color: #3b82f6;">Data Integration</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.skills {
  background-color: #000;
  color: #fff;
  padding: 100px 20px;
  text-align: center;
}

.skills h3 {
  color: #c084fc;
  font-size: 14px;
  letter-spacing: 2px;
  margin-bottom: 10px;
}

.skills h2 {
  font-size: 36px;
  font-weight: bold;
  margin-bottom: 20px;
}

.skills p {
  max-width: 700px;
  margin: 0 auto 60px;
  font-size: 18px;
  line-height: 1.8;
}

.skills-grid {
  display: flex;
  gap: 20px;
  justify-content: center;
  flex-wrap: wrap;
}

.skill-card {
  background-color: #1f1f2e;
  color: #fff;
  padding: 30px;
  border-radius: 10px;
  width: 300px;
}

.icon {
  width: 40px;
  height: 40px;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 15px;
  font-size: 20px;
}

.tags {
  margin-top: 15px;
}

.tags span {
  display: inline-block;
  color: #fff;
  padding: 5px 10px;
  border-radius: 5px;
  font-size: 13px;
  margin-right: 5px;
  margin-bottom: 5px;
}
</style>
