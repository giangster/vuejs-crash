<template>
  <div id="app">
    <Header />
    <AddTodo />
    <Todos v-bind:todos="todos" v-on:remove-todo="removeTodo" />
  </div>
</template>

<script>
import Header from "./components/layout/Header";
import AddTodo from "./components/AddTodo";
import Todos from "./components/Todos";
export default {
  name: "app",
  components: {
    Header,
    AddTodo,
    Todos
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Laundry",
          completed: true
        },
        {
          id: 2,
          title: "Dishes",
          completed: false
        },
        {
          id: 3,
          title: "Vacuuming",
          completed: false
        },
        {
          id: 4,
          title: "Groceries",
          completed: true
        }
      ]
    };
  },
  methods: {
    removeTodo(id) {
      this.todos = this.todos.filter(todo => todo.id != id);
    }
  }
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  color: #2c3e50;
  text-align: center;
  width: 80%;
  margin: auto;
  font-size: 20px;
}

.button {
  display: inline-block;
  border: none;
  background: #555;
  color: #fff;
  padding: 7px 20px;
  cursor: pointer;
}

.button:hover {
  background: #666;
}
</style>
