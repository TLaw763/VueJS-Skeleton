<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header class="container">
      <nav class="nav">
        <RouterLink class="col-md-4 text-center my-auto" to="/portfolio">Portfolio</RouterLink>
        <RouterLink class="col-md-4 text-center" to="/"><img alt="Enigmic logo" class="logo" src="@/assets/Enigmic.Logo.Long.02.png" /></RouterLink>
        <RouterLink class="col-md-4 text-center my-auto" to="/contact">Contact</RouterLink>
      </nav>
  </header>

  <RouterView />
</template>

<style>
#app {
  background-color: #261C2D;
  color: #7A7A7A;
  font-family:'Courier New', Courier, monospace;
  font-weight: 500;
}

.logo {
  max-width: 100%;
}

.nav {
  width: 100%;
  font-size: 2rem;
}

.nav a {
  text-decoration: none;
  color: #7A7A7A;;
  font-weight: 700;
}

</style>
