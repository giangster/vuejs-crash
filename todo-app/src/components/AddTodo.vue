<template>
  <div>
    <form @submit="addTodo">
      <input type="text" name="title" placeholder="Add todo" />
      <input type="submit" value="Add" class="button" />
    </form>
  </div>
</template>

<script>
import uuid from "uuid ";
export default {
  name: "AddTodo",
  data() {
    return {
      title: ""
    };
  },
  methods: {
    addTodo() {
      const newTodo = {
        id: uuid.v4(),
        title: this.title,
        completed: false
      };

      //Send to parent

      this.$emit("add-todo", newTodo);
    }
  }
};
</script>

<style scoped>
form {
  display: flex;
  margin-bottom: 20px;
}

input[type="text"] {
  flex: 10;
  padding: 5px;
  line-height: 30px;
  font-size: 20px;
}

input[type="submit"] {
  flex: 2;
  line-height: 30px;
  font-size: 20px;
}
</style>