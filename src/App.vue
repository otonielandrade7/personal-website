<template>
  <div id="app">
    <Navbar />
    <main>
      <Home />
    </main>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Home from "./components/Home.vue";

export default {
  name: "App",
  components: {
    Navbar,
    Home,
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
  --color-bg: #f5f5f5;
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
}
body {
  font-size: 2rem;
  width: 100vw;
  background-color: var(--color-bg);
}
@media (max-width: 1200px) {
}
@media (max-width: 992px) {
}
@media (max-width: 768px) {
}
@media (max-width: 480px) {
}
</style>
