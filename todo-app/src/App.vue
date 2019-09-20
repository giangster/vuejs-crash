<template>
  <div id="app">{{msg}}</div>
</template>

<script>
export default {
  name: "app",
  components: {},
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
          completed: true
        },
        {
          id: 3,
          title: "Vacuuming",
          completed: true
        },
        {
          id: 4,
          title: "Groceries",
          completed: true
        }
      ]
    };
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
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
