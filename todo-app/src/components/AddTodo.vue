<template>
  <div>
    <form>
      <input type="text" name="title" placeholder="Add todo" />
      <input type="submit" value="Add" class="button" />
    </form>
  </div>
</template>

<script>
export default {
  name: "AddTodo"
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