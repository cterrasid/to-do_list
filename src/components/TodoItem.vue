<template>
  <article class="todo-item">
    <section>
      <input type="checkbox" @change="markComplete" />
      <h1 :class="{'is-complete':todo.completed}">{{todo.title}}</h1>
    </section>
    <button @click="$emit('del-todo', todo.id)" class="del">X</button>
  </article>
</template>
<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
    },
  },
};
</script>

<style scoped>
.todo-item {
  align-items: center;
  background: var(--veryLightGrey);
  border-bottom: 1px var(--lightGrey) dotted;
  display: flex;
  padding: 10px;
}

.is-complete {
  text-decoration: line-through;
  color: var(--darkPurple);
}

section {
  align-items: center;
  display: flex;
  width: 90%;
  justify-content: flex-start;
}

section > h1 {
  padding: 0 10px;
}

.del {
  background: var(--purple);
  border-radius: 50%;
  border: none;
  color: var(--white);
  cursor: pointer;
  float: right;
  font-weight: bold;
  height: 30px;
  padding: 5px 9px;
  width: 30px;
}
</style>