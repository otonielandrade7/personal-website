<template>
  <header id="navbar" class="navbar">
    <div class="navbar-logo-container">
      <img
        loading="lazy"
        src="@/assets/logo.png"
        class="navbar-logo-img"
        alt="Logo de Otoniel Andrade"
        width="50"
        height="50"
      />
    </div>
    <div :class="{ hidden: mobileNavbar }" class="toggle-container">
      <button
        aria-label="Menú icon toggler"
        :class="{ hidden: mobileNavbar }"
        v-on:click="toggleNavbar()"
        class="toggle"
      >
        <svg
          version="1.1"
          id="Layer_1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          x="0px"
          y="0px"
          viewBox="0 0 50 50"
          enable-background="new 0 0 50 50"
          xml:space="preserve"
        >
          <path
            fill="#231F20"
            d="M8.667,15h30c0.552,0,1-0.447,1-1s-0.448-1-1-1h-30c-0.552,0-1,0.447-1,1S8.114,15,8.667,15z"
          />
          <path
            fill="#231F20"
            d="M8.667,37h30c0.552,0,1-0.447,1-1s-0.448-1-1-1h-30c-0.552,0-1,0.447-1,1S8.114,37,8.667,37z"
          />
          <path
            fill="#231F20"
            d="M8.667,26h30c0.552,0,1-0.447,1-1s-0.448-1-1-1h-30c-0.552,0-1,0.447-1,1S8.114,26,8.667,26z"
          />
        </svg>
      </button>
    </div>
    <nav id="nav" class="navbar-nav" :class="{ 'open-mobile': mobileNavbar }">
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
        <li class="navbar-item darkmode-toggle-container">
          <input
            v-model="darkmodeTheme"
            type="checkbox"
            name="checkbox"
            id="checkbox"
            v-on:change="themeToggler()"
          />
          <label class="darkmode-toggle" for="checkbox"> </label>
        </li>
      </ul>
    </nav>
    <div class="white-div"></div>
  </header>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      mobileNavbar: false,
      theme: localStorage.getItem("theme"),
      darkmodeTheme: false,
      myDocument: document.getElementById("app"),
    };
  },
  methods: {
    toggleNavbar: function () {
      this.mobileNavbar = !this.mobileNavbar;
    },
    check() {
      if (this.theme === "dark") {
        this.darkmodeTheme = true;
      }
      if (this.theme === "light" || this.theme === null) {
        this.darkmodeTheme = false;
      }
      this.themeToggler();
    },
    themeToggler() {
      if (this.darkmodeTheme) {
        document.querySelector("body").classList.remove("light-mode");
        document.querySelector("body").classList.add("dark-mode");
        localStorage.setItem("theme", "dark");
      } else if (!this.darkmodeTheme) {
        document.querySelector("body").classList.remove("dark-mode");
        document.querySelector("body").classList.add("light-mode");
        localStorage.setItem("theme", "light");
      }
    },
  },
  created() {
    this.check();
    document.body.addEventListener(
      "click",
      () => {
        if (this.mobileNavbar) {
          this.mobileNavbar = !this.mobileNavbar;
        }
      },
      true
    );
  },
};
</script>

<style>
.navbar {
  display: flex;
  padding: 0 2rem;
  align-items: center;
  height: 6.5rem;
  background-color: var(--glass);
  box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  backdrop-filter: blur(10px);
}
.navbar > * {
  margin: 1rem 0;
}
.hidden {
  display: none;
}
.toggle {
  width: 5rem;
}
.toggle-container {
  display: none;
  order: 3;
  width: 4.5rem;
}
.toggle-container svg path {
  fill: var(--color-text-default);
}
.white-div {
  order: 4;
  width: 4.5rem;
}
.navbar-logo-container {
  order: 1;
  width: 5rem;
  min-width: 4.5rem;
  height: auto;
  display: flex;
}
.navbar-logo-img {
  width: 100%;
  height: auto;
}
.toggle {
  border: none;
  background-color: transparent;
  text-decoration: underline solid 1px black;
}
#checkbox {
  display: none;
}
.navbar-list .navbar-item.darkmode-toggle-container {
  display: flex;
  justify-content: center;
  margin: 0 0 0 auto;
}
.darkmode-toggle {
  display: flex;
  width: 5rem;
  padding: 0.3rem;
  margin: 0.5rem;
  border-radius: 100px;
  cursor: pointer;
  justify-content: flex-start;
  background-color: var(--toggle-bg);
  box-shadow: 1px 1px 1px rgba(0, 0, 0, 0.2) inset;
  align-items: center;
}
.darkmode-toggle:before {
  background-color: var(--color-primary);
  content: "";
  box-shadow: 1px 1px 1px rgba(0, 0, 0, 0.2);
  width: 1.5rem;
  height: 1.5rem;
  border-radius: 100%;
  transform: scale(1.8);
  transition: all 0.2s;
}
#checkbox:checked ~ .darkmode-toggle:before {
  transform: translateX(2.6rem) scale(1.8);
  align-self: center;
}
.navbar-nav {
  order: 2;
  margin-left: 2rem;
  width: 100%;
}
.navbar-list {
  display: flex;
  list-style-type: none;
  align-items: center;
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
  .navbar {
    height: auto;
  }
  .navbar-logo-container {
    width: 4.5rem;
    align-self: flex-start;
  }
  .navbar-nav {
    margin: 0 auto;
    display: none;
  }
  .toggle-container {
    display: block;
    position: absolute;
    right: 2rem;
    align-self: flex-start;
  }
  .open-mobile {
    display: block;
    height: auto;
  }
  .open-mobile > .navbar-list {
    flex-direction: column;
    height: auto;
    text-align: center;
  }
  .open-mobile > .navbar-list > .navbar-item {
    transition: all 0.2s;
    margin: 0;
  }
  .open-mobile > .navbar-list > .navbar-item:first-child {
    margin: 1.5rem 0 2rem;
  }
  .open-mobile > .navbar-list > .navbar-item {
    margin: 2rem 0;
  }
}
@media (max-width: 480px) {
}
</style>