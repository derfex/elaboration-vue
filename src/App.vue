<script lang="ts" setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header class="app-header">
    <img alt="Vue logo" class="app-logo" src="@/assets/logo.svg" />

    <div class="app-wrapper">
      <HelloWorld msg="You did it!" />

      <nav class="app-nav">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/works">Works</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
.app-header {
  line-height: 1.5;
}

.app-logo {
  display: block;
  margin: 0 auto 2rem;
  width: 125px;
  height: 125px;
}

.app-nav {
  margin-top: 2rem;
  width: 100%;
  font-size: 12px;
  text-align: center;
}

.app-nav a.router-link-exact-active {
  color: var(--color-text);
}

.app-nav a.router-link-exact-active:hover {
  background-color: transparent;
}

.app-nav a {
  display: inline-block;
  border-left: 1px solid var(--color-border);
  padding: 0 1rem;
}

.app-nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  .app-header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .app-logo {
    margin: 0 2rem 0 0;
  }

  .app-header .app-wrapper {
    display: flex;
    flex-wrap: wrap;
    place-items: flex-start;
  }

  .app-nav {
    margin-top: 1rem;
    margin-left: -1rem;
    padding: 1rem 0;
    font-size: 1rem;
    text-align: left;
  }
}
</style>
