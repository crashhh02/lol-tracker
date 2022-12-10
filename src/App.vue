<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import Sidebar from '@/components/Sidebar/Sidebar.vue'
</script>

<template>
  <Sidebar/>
  <RouterView />
</template>

<style >
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}
#app {
  display: flex;
}

main {
  flex: 1 1 0;
  padding: 2rem;
}

@media (max-width: 768px) {
  main {
    padding-left: 6rem;
  }
}
</style>
