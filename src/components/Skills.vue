<template>
  <div id="skills">
    <div class="skills-container first-container">
      <div><p>Tengo experiencia trabajando con:</p></div>
      <div class="skills-grid">
        <div class="skill-card html-card"><p>HTML</p></div>
        <div class="skill-card css-card"><p>CSS</p></div>
        <div class="skill-card js-card"><p>JavaScript</p></div>
        <div class="skill-card vue-card"><p>Vue.js</p></div>
        <div class="skill-card firebase-card"><p>Firebase</p></div>
        <div class="skill-card sql-card"><p>SQL</p></div>
        <div class="skill-card mongo-card"><p>Mongo DB</p></div>
        <div class="skill-card rest-card"><p>REST</p></div>
      </div>
    </div>
    <div class="skills-container">
      <div><p>Soft skills:</p></div>
      <div class="skills-grid">
        <div class="skill-card"><p>Puntualidad</p></div>
        <div class="skill-card"><p>Empatía</p></div>
        <div class="skill-card"><p>Comunicación</p></div>
        <div class="skill-card"><p>Rápido aprendizaje</p></div>
        <div class="skill-card"><p>Trabajo en equipo</p></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
#skills {
  height: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: var(--color-base);
  flex-direction: column;
  padding: 0 0 10rem 0;
}
.first-container {
  margin: 10rem 0 3rem;
}
.skills-container {
  padding: 3.5rem 3rem;
  border: var(--color-border) 1px solid;
  width: 65%;
  max-width: 65%;
  border-radius: var(--border-radius-default);
  box-shadow: 3px 3px 20px rgba(0, 0, 0, 0.2);
  background-color: var(--color-base);
}
.skills-grid {
  margin: 2.5rem 0;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
  grid-auto-rows: minmax(4rem, auto);
}
.skill-card {
  border-radius: 2px;
  border: var(--color-border) 1px solid;
  padding: 0 1rem;
  cursor: default;
  transition: all 0.1s;
  text-transform: center;
  border-left: 8px var(--color-primary) solid;
  display: flex;
}
.skill-card > p {
  align-self: center;
}

.skill-card:hover {
  box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.1);
}
.html-card {
  border-left: 8px #e34f26 solid;
}
.css-card {
  border-left: 8px #016cb4 solid;
}
.js-card {
  border-left: 8px #e8d44d solid;
}
.firebase-card {
  border-left: 8px #ffcc2c solid;
}
.vue-card {
  border-left: 8px #31475e solid;
}
.mongo-card {
  border-left: 8px #79b866 solid;
}
.rest-card {
  border-left: 8px #c01c81 solid;
}
@media (max-width: 1200px) {
}
@media (max-width: 992px) {
  .skills-container {
    width: 75%;
    max-width: 75%;
    margin: 5rem 0 2rem;
  }
}
@media (max-width: 768px) {
  .skills-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  .skills-container {
    width: 80%;
    max-width: 80%;
  }
}
@media (max-width: 480px) {
  .skills-grid {
    grid-template-columns: repeat(1, 1fr);
  }
  .skills-container {
    width: 90%;
    max-width: 90%;
  }
}
</style>