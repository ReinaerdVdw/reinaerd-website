<template>
  <section id="contact" class="contact">
    <div class="header">
      <h3>GET IN TOUCH</h3>
      <h2>Let's Work Together</h2>
      <p>
        Interested in working together? Feel free to reach out to discuss your Power Platform project.
      </p>
    </div>

    <div class="content">
      <div class="info">
        <div class="row">
          <div class="icon"><svg
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    fill="currentColor"
    viewBox="0 0 24 24"
  >
    <path
      d="M20 4H4c-1.1 0-2 .9-2 
      2v12c0 1.1.9 2 2 
      2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 
      2v.01L12 13 4 6.01V6h16zM4 
      18V8l8 5 8-5v10H4z"
    />
  </svg></div>
          <div>
            <strong>Email</strong><br />
            <span>reinaerd.vandewalle@example.com</span>
          </div>
        </div>

        <div class="social">
          <strong>Connect with me</strong>
          <div class="social-icons">
            <a href="https://github.com/ReinaerdVdw" target="_blank"><svg
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    fill="currentColor"
    viewBox="0 0 24 24"
  >
    <path
      d="M12 0C5.373 0 0 5.373 0 12c0 5.303 
      3.438 9.8 8.205 11.387.6.113.82-.26.82-.577
      0-.285-.01-1.04-.015-2.04-3.338.726-4.042
      -1.61-4.042-1.61-.546-1.387-1.333-1.756-1.333-1.756
      -1.09-.745.083-.729.083-.729 1.205.085 1.84 1.236
      1.84 1.236 1.07 1.834 2.809 1.304 3.495.997.108
      -.775.42-1.305.762-1.605-2.665-.3-5.466-1.334-5.466
      -5.931 0-1.31.467-2.381 1.235-3.221-.124-.303
      -.535-1.524.117-3.176 0 0 1.008-.322 3.3
      1.23.957-.266 1.98-.399 3-.404 1.02.005 2.043.138
      3 .404 2.29-1.552 3.297-1.23 3.297-1.23.653
      1.653.242 2.874.118 3.176.77.84 1.233 1.911
      1.233 3.221 0 4.609-2.804 5.628-5.475
      5.921.431.372.815 1.102.815 2.222 0 1.606
      -.014 2.896-.014 3.286 0 .319.218.694.825.576C20.565
      21.796 24 17.299 24 12c0-6.627-5.373-12-12-12z"
    />
  </svg></a>
            <a href="https://www.linkedin.com/in/reinaerd-vandewalle-0484271ba/" target="_blank"><svg
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    viewBox="0 0 24 24"
    fill="currentColor"
  >
    <path
      d="M19 0h-14c-2.761 0-5 2.239-5 
      5v14c0 2.761 2.239 5 5 5h14c2.761 
      0 5-2.239 5-5v-14c0-2.761-2.239-5-5-5zm-11 
      19h-3v-10h3v10zm-1.5-11.268c-.966 
      0-1.75-.784-1.75-1.75s.784-1.75 
      1.75-1.75 1.75.784 
      1.75 1.75-.784 1.75-1.75 
      1.75zm13.5 
      11.268h-3v-5.604c0-1.337-.026-3.059-1.865-3.059-1.868 
      0-2.155 1.459-2.155 2.968v5.695h-3v-10h2.881v1.367h.041c.401-.76 
      1.379-1.559 2.837-1.559 3.033 
      0 3.595 1.996 3.595 4.59v5.602z"
    />
  </svg></a>
            <a href="mailto:reinaerd.vdw@gmail.com"><svg
    xmlns="http://www.w3.org/2000/svg"
    width="24"
    height="24"
    fill="currentColor"
    viewBox="0 0 24 24"
  >
    <path
      d="M20 4H4c-1.1 0-2 .9-2 
      2v12c0 1.1.9 2 2 
      2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 
      2v.01L12 13 4 6.01V6h16zM4 
      18V8l8 5 8-5v10H4z"
    />
  </svg></a>
          </div>
        </div>

       
      </div>

      <div class="form">
        <form @submit.prevent="submitForm">
          <input v-model="name" type="text" placeholder="Your Name" />
          <input v-model="email" type="email" placeholder="Your Email" />
          <textarea v-model="message" placeholder="Your Message"></textarea>
          <button type="submit">Send Message</button>
        </form>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const name = ref('')
const email = ref('')
const message = ref('')

function submitForm() {
  console.log('Sending message:', name.value, email.value, message.value)
  alert('Message sent!')
  name.value = ''
  email.value = ''
  message.value = ''
}
</script>

<style scoped>
.contact {
  background-color: #000;
  color: #fff;
  padding: 100px 20px;
}

.header {
  text-align: center;
  margin-bottom: 60px;
}

.header h3 {
  color: #c084fc;
  font-size: 14px;
  letter-spacing: 2px;
  margin-bottom: 10px;
}

.header h2 {
  font-size: 36px;
  font-weight: bold;
  margin-bottom: 20px;
}

.header p {
  font-size: 18px;
  line-height: 1.6;
  max-width: 700px;
  margin: 0 auto;
}

.content {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 40px;
  max-width: 1100px;
  margin: 0 auto;
}

.info {
  flex: 1;
  min-width: 300px;
}

.row {
  margin-bottom: 30px;
  display: flex;
  align-items: center;
  gap: 12px;
}

.icon {
  background-color: #7c3aed;
  padding: 10px;
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.row span {
  color: #ccc;
}

.social {
  margin-bottom: 30px;
}

.social-icons {
  margin-top: 10px;
  display: flex;
  gap: 10px;
}

.social-icons a {
  border: 1px solid #c084fc;
  border-radius: 6px;
  padding: 8px;
  display: inline-flex;
  text-decoration: none;
}

.video strong {
  display: block;
  margin-bottom: 10px;
}

.iframe-wrapper {
  border-radius: 10px;
  overflow: hidden;
}

.form {
  flex: 1;
  min-width: 300px;
  background-color: #1f1f2e;
  padding: 30px;
  border-radius: 10px;
}

.form form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.form input,
.form textarea {
  background: #333;
  border: none;
  color: #fff;
  padding: 10px;
  border-radius: 5px;
}

.form button {
  background-color: #c084fc;
  color: #fff;
  border: none;
  padding: 12px;
  border-radius: 5px;
  font-weight: bold;
  cursor: pointer;
}
</style>
