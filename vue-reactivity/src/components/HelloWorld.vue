<template>
<button @click="increment">count is: {{ count }}</button>
  <input v-model="text" placeholder="type here">
  <p>{{ text }}</p>
</template>

<script setup>
import { ref, transformVNodeArgs } from 'vue'

const count = ref(0)
//This adds a counter
function increment(){
  count.value++
}

const text = ref('')

let id = 0
function addTodo(){
  todos.value.push({ id: id++, text: newTodo.value })
  newTodo.value = ''
}

function removeTodo(todo) {
  todos.value = todos.value.filter((t) => t !== todo)
}

</script>

<style scoped>

</style>