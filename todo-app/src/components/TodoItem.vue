<template>
  <div class="todo-item" v-bind:class="{'is-completed':todo.completed}">
    <input type="checkbox" v-on:change="markComplete" />
    {{todo.title}}
    <button @click="$emit('remove-todo', todo.id)" class="remove-todo">&#10005;</button>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
    }
  }
};
</script>

<style scoped>
.todo-item {
  background: #f4f4f4;
  padding: 10px;
  border-bottom: 1px #ccc dotted;
  justify-content: space-between;
}

.is-completed {
  text-decoration: line-through;
}

.remove-todo {
  float: right;
  background: #b32d2d;
  width: 20px;
  height: 20px;
  border: none;
  border-radius: 50%;
  color: white;
}
</style>