<template>
  <div id="contact">
    <div class="contact-container">
      <div class="contact-title">
        <h1>Contáctame</h1>
      </div>
      <div class="contact-info">
        <div class="contact-media-card">
          <h2>Redes sociales</h2>
          <ul class="contact-list">
            <li class="contact-item">
              <a
                target="_blank"
                class="contact-link"
                href="https://www.linkedin.com/in/otonielandrade7/"
                >LinkedIn
              </a>
            </li>
            <li class="contact-item">
              <a
                target="_blank"
                class="contact-link"
                href="https://twitter.com/otonielandrade7/"
                >Twitter</a
              >
            </li>
            <li class="contact-item">
              <a
                target="_blank"
                class="contact-link"
                href="https://instagram.com/otonielandrade7"
                >Instagram</a
              >
            </li>
          </ul>
        </div>
        <div class="contact-others-card">
          <h2>Otros</h2>
          <ul class="contact-list">
            <li class="contact-item">
              <a
                class="contact-link mail"
                href="mailto:otonielandrade7@gmail.com"
                >Correo electrónico</a
              >
            </li>
            <li class="contact-item">
              <a
                target="_blank"
                class="contact-link"
                href="https://github.com/otonielandrade7"
                >GitHub</a
              >
            </li>
            <li class="contact-item">
              <a
                target="_blank"
                class="contact-link"
                href="https://codepen.io/otonielandrade7"
                >CodePen</a
              >
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="message">
      <small
        >Hecho por <a href="#home">Otoniel Andrade</a> con
        <a href="#skills">Vue.js 💚</a></small
      >
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.message {
  margin: 3rem 0 0 0;
  display: flex;
}
.message small {
  margin: 0 auto;
}
.message small a {
  color: var(--color-text-default);
  text-decoration: none;
}
.message small a:hover {
  color: var(--color-text-default);
  text-decoration: underline;
}
#contact {
  height: 100%;
  padding: 3rem 5rem 3rem;
}
.contact-container {
  width: auto;
}
.contact-info {
  display: grid;
  justify-content: center;
  grid-template-columns: repeat(2, 1fr);
  grid-auto-columns: minmax(1fr, 10rem);
  gap: 3rem;
}
.contact-title {
  margin: 0 0 2rem 0;
}

.social-media-card,
.social-others-card {
  width: 75%;
}
.contact-list {
  list-style-type: none;
  border-left: 2px var(--color-primary) solid;
  padding-left: 1rem;
}
.contact-item {
  margin: 1rem 0;
  display: flex;
  gap: 5px;
}
.contact-item a {
  text-decoration: none;
  color: var(--color-text);
}
.contact-item a:hover {
  text-decoration: underline;
}
.contact-media-image {
  fill: yellowgreen;
}
@media (max-width: 1200px) {
}
@media (max-width: 992px) {
}
@media (max-width: 768px) {
}
@media (max-width: 480px) {
  .contact-info {
    grid-template-columns: repeat(1, 1fr);
    grid-auto-columns: minmax(1fr, 10rem);
  }
}
</style>
