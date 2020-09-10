<template>
  <form @submit="addTodo">
    <input type="text" v-model="title" name="title" placeholder="Add Todo..." />
    <input type="submit" value="Submit" class="btn" />
  </form>
</template>

<script>
export default {
  name: "AddTodo",
  data() {
    return {
      title: "",
    };
  },
  methods: {
    addTodo(e) {
      e.preventDefault();
      const newTodo = {
        title: this.title,
        completed: false,
      };
      this.$emit("add-todo", newTodo);
      this.title = "";
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
  margin: 30px 10px 20px 10px;
}

input[type="text"] {
  border: none;
  border-bottom: 2px solid var(--black);
  flex: 10;
  margin-right: 10px;
  padding: 5px;
}

input[type="submit"] {
  flex: 2;
}
</style>