<template>
  <div class="container">
    <input v-model="task" type="text" />
    <button @click="createTask">Create</button>
    <TodoList :tasks="tasks" />
  </div>
</template>

<script setup>
import { reactive, ref } from "@vue/reactivity";
import TodoList from "../components/TodoList.vue";

const task = ref("");
let tasks = reactive([
  { id: 1, name: "cooking" },
  { id: 2, name: "eating" },
  { id: 3, name: "dancing" },
]);

const createTask = () => {
  const newId = tasks.length;
  tasks.push({ id: newId, name: task.value });
};
</script>

<style lang="scss" scoped></style>
