<template>
  <div>
    <TodoForm @added="addToList" />

    <ul>
      <TodoListItem v-for="(item, index) in todos" :key="index" :todo="item" />
    </ul>
  </div>
</template>

<script setup>
import TodoForm from "./TodoForm.vue";
import TodoListItem from "./TodoListItem.vue";
import { ref } from "vue";

const todos = ref([
  {
    id: 1,
    text: "Learn React",
  },
  {
    id: 2,
    text: "Learn Vue",
  },
]);

function addToList(data) {
  todos.value = [...todos.value, { id: todos.value.length + 1, text: data }];
}
</script>

<style lang="scss" scoped></style>
