<template>
  <div id="app">
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
  }
};
</script>

<style>
.light-mode {
  --border-radius-default: 4px;
  --color-primary: #367eff;
  --color-text-default: #3c484e;
  --color-text-secondary: #999;
  --color-border: #d8d7c7;
  --color-bg: #eff3f5;
  --color-base: #fff;
  --glass: rgba(255, 255, 255, 0.75);
  --toggle-bg: #d8d7c7;
}
.dark-mode {
  --color-primary: #2b70f1;
  --color-base: #212e36;
  --color-base-opacity: #383737;
  --color-secondary: #eed625;
  --color-border: #1f2930;
  --color-bg: #192229;
  --color-text-default: rgb(239, 243, 245);
  --color-text-secondary: #eee;
  --color-white: #fff;
  --glass: rgba(33, 46, 54, 0.75);
  --toggle-bg: #094977;
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
  overflow-x: hidden;
}
h1 {
  font-weight: 600;
}
h2 {
  font-weight: normal;
}
body {
  font-size: 2rem;
  width: 100vw;
  max-width: 100vw;
  background-color: var(--color-bg);
  color: var(--color-text-default);
}
main > #skills {
  padding-top: 7rem;
}
footer {
  max-height: auto;
  position: relative;
  bottom: 0;
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
