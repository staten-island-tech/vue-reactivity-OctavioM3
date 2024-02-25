<template>
 <header>
  <h1>The Shop</h1>
  </header>
  
  <RouterView />
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<style scoped>

header {
    display: flex;
    place-items: center;
    flex-wrap: wrap;
    text-align: center;
  }
h1 {
  text-align: center;
}
</style>