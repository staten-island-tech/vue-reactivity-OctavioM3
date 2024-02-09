<template>
<button @click="increment">count is: {{ count }}</button>
  <input v-model="text" placeholder="type here">
  <p>{{ text }}</p>
  
  <form @submit.prevent="addTodo">
  <input v-model="newTodo">
  <button>Add Todo</button>
  </form>
  <li v-for="todo in todos" :key="todo.id">
    {{ todo.text }}
  </li>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)
//This adds a counter
function increment(){
  count.value++
}

const text = ref('')

let id = 0

const newTodo = ref('')
const todos = ref([
  {},
])
function addTodo(){
  todos.value.push({ id: id++, text: newTodo.value })
  newTodo.value = ''
}


</script>

<style scoped>

</style>