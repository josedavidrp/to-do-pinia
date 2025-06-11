<template>
  <div>
    <form @submit.prevent="addItemAndClear(todo)">
      <input v-model="todo" type="text" /> <button>Añadir</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { useTodoListStore } from '@/stores/todoList.js'
const todo = ref('')
const store = useTodoListStore()

function addItemAndClear(item) {
  if (item.length === 0) {
    return
  }
  store.addTodo(item)
  todo.value = ''
}
</script>

<style scoped></style>
