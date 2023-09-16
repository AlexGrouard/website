<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <h1 class="logo">Alex GROUARD</h1>
    <div class="wrapper">
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/skills">Skill</RouterLink>
        <RouterLink to="/projects">Projects</RouterLink>
        <RouterLink to="/Resume">Resume</RouterLink>
        <RouterLink to="/contact">Contact</RouterLink>
      </nav>
    </div>
  </header>
<div class="main">
  <RouterView />
</div>
</template>

<style scoped>

header {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  line-height: 1.5;
  max-height: 100vh;
}
.main {
  display: flex;
  align-items: center;
  justify-content: center;
}

nav {
  width: 100%;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

</style>
