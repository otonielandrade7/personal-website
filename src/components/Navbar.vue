<template>
  <header id="navbar" class="navbar">
    <div class="navbar-logo-container">
      <img src="@/assets/logo.webp" class="navbar-logo-img" alt="" />
    </div>
    <nav class="navbar-nav">
      <ul class="navbar-list">
        <li class="navbar-item">
          <a class="navbar-link" href="#home">Inicio</a>
        </li>
        <li class="navbar-item">
          <a class="navbar-link" href="#skills">Habilidades</a>
        </li>
        <li class="navbar-item">
          <a class="navbar-link" href="#contact">Contacto</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
.navbar {
  display: flex;
  padding: 0 2rem;
  align-items: center;
  height: 6.5rem;
  background-color: rgba(255, 255, 255, 0.75);
  box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  backdrop-filter: blur(10px);
}
.navbar > * {
  margin: 1rem 0;
}
.navbar-logo-container {
  width: 5rem;
  min-width: 4.5rem;
  height: auto;
  display: flex;
}
.navbar-logo-img {
  width: 100%;
  height: auto;
}
.navbar-nav {
  margin-left: 2rem;
}
.navbar-list {
  display: flex;
  list-style-type: none;
}

.navbar-list .navbar-item {
  margin: 0 0.5rem;
}
.navbar-list .navbar-link {
  text-decoration: none;
  padding: 1rem 1.5rem;
  border-radius: var(--border-radius-default);
  color: var(--color-text-default);
}
.navbar-link:hover {
  text-decoration: underline;
}

@media (max-width: 1200px) {
}
@media (max-width: 992px) {
  .navbar-logo-container {
    width: 5rem;
  }
}
@media (max-width: 768px) {
  .navbar-logo-container {
    width: 4.5rem;
  }
  .navbar-nav {
    margin-left: 0.5rem;
  }
}
@media (max-width: 480px) {
}
</style>