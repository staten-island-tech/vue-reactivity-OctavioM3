<template>
<button @click="increment">count is: {{ count }}</button>
  <input v-model="text" placeholder="type here">
  <p>{{ text }}</p>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)
//This adds a counter
function increment(){
  count.value++
}

const text = ref('')

</script>

<style scoped>

</style>