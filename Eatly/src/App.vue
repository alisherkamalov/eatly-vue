<script setup>
import { RouterLink, RouterView } from 'vue-router'
import navigation from './components/TheNav.vue'
</script>

<template>
  <nav>
    <navigation></navigation>
  </nav>
  <RouterView />
</template>

<style scoped>

</style>
