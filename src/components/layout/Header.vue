<template>
  <header>
    <nav>
      <h1>Todo List</h1>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
header {
  background: var(--black);
  text-align: center;
  padding: 10px;
}

nav {
  align-items: center;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
}

h1, a {
  color: var(--white);
  text-decoration: none;
}

h1 {
  justify-self: flex-start;
}

</style>