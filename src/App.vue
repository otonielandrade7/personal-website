<template>
  <div id="app">
    <div class="warn">Responsive design soon.</div>
    <Navbar />
    <main>
      <Home />
      <Skills />
    </main>
    <footer>
      <Contact />
    </footer>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Home from "./components/Home.vue";
import Skills from "./components/Skills.vue";
import Contact from "./components/Contact.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Home,
    Contact,
    Skills,
  },
};
</script>

<style>
:root {
  --border-radius-default: 4px;
  --color-primary: #367eff;
  --color-text-default: #3c484e;
  --color-text-secondary: #999;
  --color-border: #d8d7c7;
  --color-bg: #eff3f5;
  --color-base: #fff;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  font-size: 62.5%;
  font-family: "Roboto", sans-serif;
  scroll-behavior: smooth;
}
body {
  font-size: 2rem;
  max-width: 100vw;
  background-color: var(--color-bg);
}
main > #skills {
  padding-top: 7rem;
}
footer {
  height: 50vh;
  position: relative;
  bottom: 0;
}
  .warn {
    display: none;
  }
@media (max-width: 1200px) {
}
@media (max-width: 992px) {
}
@media (max-width: 768px) {
  .warn {
    display: block;
  }
}
@media (max-width: 480px) {
}
</style>
