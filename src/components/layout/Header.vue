<template>
  <header>
      <h1>Todo List</h1>
    <nav>
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

a {
  padding: 5px
}

a:active, a:focus {
  font-weight: bold;
}

h1, a {
  color: var(--white);
  text-decoration: none;
}

h1 {
  justify-self: flex-start;
}

</style>