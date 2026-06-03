<script setup>
import { ref, computed } from 'vue'
import Home from './Home.vue'
import GameDev from './Game.vue'
import Series from './Series.vue'
import Edit from './edit.vue'

const routes = {
  '/': Home,
  '/game': GameDev,
  '/series': Series,
  '/edit': Edit
}

const currentPath = ref(window.location.hash)

window.addEventListener('hashchange', () => {
  currentPath.value = window.location.hash
})

const currentView = computed(() => {
  return routes[currentPath.value.slice(1) || '/'] || NotFound
})
</script>

<template>
  <component :is="currentView" />
</template>