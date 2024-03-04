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
  color: dodgerblue;
  background-color: black;
  padding: 5%;
  margin: 2%;
}
</style>