<template>
  <div>
    <HelloWorld
    v-for="todo in todos" 
    :key="todo.id"
    ;Todo = "todo"
    />
  </div>
</template>

<script setup>
import HelloWorld from '@/components/HelloWorld.vue';

</script>

<style  scoped>

</style>