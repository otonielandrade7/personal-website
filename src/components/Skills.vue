<template>
  <div id="skills">
    <div class="skills-container">
      <div class="lang-card"><p>HTML</p></div>
      <div class="lang-card"><p>CSS</p></div>
      <div class="lang-card"><p>JavaScript</p></div>
      <div class="lang-card"><p>Firebase</p></div>
      <div class="lang-card"><p>Vue.js</p></div>
      <div class="lang-card"><p>SQL</p></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
#skills {
  height: 100vh;
  border: solid 1px red;
  display: flex;
  justify-content: center;
  align-items: flex-start;
}
.skills-container {
  padding: 3.5rem 3rem;
  display: grid;
  margin: 10rem;
  border: var(--color-border) 1px solid;
  width: 65%;
  max-width: 65%;
  border-radius: var(--border-radius-default);
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
  box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.1);
  background-color: var(--color-base);
  grid-auto-rows: 4rem;
}
.lang-card {
  border-radius: 2px;
  border: var(--color-border) 1px solid;
  padding: 0 1rem;
  cursor: default;
  transition: all 0.1s;
  text-transform: center;
  border-left: 8px var(--color-primary) solid;
  display: flex;
}
.lang-card > p {
  align-self: center;
}

.lang-card:hover {
  border: var(--color-primary) 1px solid;
  border-left: 8px var(--color-primary) solid;
  box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.1);
}
</style>