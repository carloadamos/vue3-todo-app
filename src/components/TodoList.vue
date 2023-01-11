<template>
  <div>Todolist</div>
  <ul>
    <li v-for="task in tasks" :key="task.id">{{ task.name }}</li>
  </ul>
</template>

<script setup>
const props = defineProps({
  tasks: Array,
});
</script>

<style lang="scss" scoped></style>
