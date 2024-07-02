<script setup>
import TheTitle from './components/TheTitle.vue'
import CheckerList from './components/CheckerList.vue'
import ThePassword from './components/ThePassword.vue'
</script>

<template>
  <div class="page-container">
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
    <div class="wrapper">
      <TheTitle/>
    </div>
  </header>
</div>

  <main>
    <ThePassword/>
    <CheckerList/>
  </main>
</template>

<style scoped>

.page-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh; /* Esto hace que el contenedor tenga el tamaño de la ventana visible */
  padding: 0;
  margin: 0;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
