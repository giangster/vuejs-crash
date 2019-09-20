<template>
  <div v-bind:todo="todo">
    <h3>{{todo.title}}</h3>
    <div>{{todo.completed}}</div>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"]
};
</script>

<style scoped>
</style>