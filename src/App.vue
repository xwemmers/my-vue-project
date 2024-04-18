<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/heroes">Superheroes</RouterLink>
    </nav>

  <RouterView />

</template>

<style scoped>

nav
{
  background-color: blue;
  text-align: center;
  padding: 20px;
}

a
{
  color: white;
  margin: 10px;
}

</style>
