<template>
 <header>
  <h1>Casual Clothing</h1>
  </header>

  <RouterView />
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<style scoped>
header {
  text-align: center;
}
template {
  background-color: dimgrey;
}
</style>