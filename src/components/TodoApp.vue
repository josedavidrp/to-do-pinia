<template>
  <div class="todo-app">
    <h1>Lista de tareas</h1>
    <todo-form />
    <todo-list />
  </div>
</template>

<script setup>
import TodoForm from '@/components/TodoForm.vue'
import TodoList from '@/components/TodoList.vue'
</script>

<style scoped></style>
