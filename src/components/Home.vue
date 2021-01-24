<template>
  <div id="home">
    <div class="presentation-container">
      <div class="presentation-photo-container">
        <img
          class="presentation-photo"
          src="@/assets/profile-oto.jpg"
          alt="Fotografía de Otoniel Andrade"
        />
      </div>
      <div class="presentation-description">
        <h1 class="gretting">Hola, soy Otoniel Andrade 👋</h1>
        <h2 class="gretting-tagline">Frontend web developer</h2>
        <p>
          Soy un desarrollador web frontend salvadoreño dedicado, con amor por la
          tecnología y el aprendizaje continuo. 👨‍💻
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
#home {
  height: calc(100vh - 6.5rem);
  display: flex;
  justify-content: center;
  align-items: center;
}
.presentation-container {
  border: 1px solid var(--color-border);
  border-radius: var(--border-radius-default);
  height: 30rem;
  width: auto;
  max-width: 65%;
  padding: 0 3rem;
  display: flex;
  align-items: center;
  column-gap: 3rem;
  background-color: var(--color-base);
  box-shadow: 1px 1px 20px rgba(0, 0, 0, 0.1);
}
.presentation-container .gretting-tagline {
  color: var(--color-primary);
}
.presentation-photo-container {
  width: 20rem;
  min-width: 15rem;
  height: auto;
}
.presentation-photo {
  width: 100%;
  height: auto;
  border-radius: 100%;
}
</style>