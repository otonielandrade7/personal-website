<template>
  <div id="contact">
    <div class="contact-container">
      <div class="contact-title">
        <h2>Contáctame</h2>
      </div>
      <div class="contact-info">
        <div class="contact-media-card">
          <h3>Redes sociales</h3>
          <ul class="contact-list">
            <li class="contact-item">
              <a href="https://www.linkedin.com/in/otonielandrade7/"
                >LinkedIn
              </a>
            </li>
            <li class="contact-item">
              <a href="https://twitter.com/otonielandrade7/">Twitter</a>
            </li>
            <li class="contact-item">
              <a href="https://instagram.com/otonielandrade7">Instagram</a>
            </li>
          </ul>
        </div>
        <div class="contact-others-card">
          <h3>Otros</h3>
          <ul class="contact-list">
            <li class="contact-item">
              <a href="mailto:otonielandrade7@gmail.com"
                >otonielandrade7@gmail.com</a
              >
            </li>
            <li class="contact-item">
              <a href="https://github.com/otonielandrade7">GitHub</a>
            </li>
            <li class="contact-item">
              <a href="https://codepen.io/otonielandrade7">CodePen</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
#contact {
  height: 100%;
  padding: 3rem 5rem 3rem;
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
}
.contact-item {
  margin: 1rem 0;
}
.contact-item a {
  text-decoration: none;
  color: var(--color-text);
}
.contact-item a:hover {
  text-decoration: underline;
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