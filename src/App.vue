<template>
  <div id="app">
    <Header />
    <router-view/>
  </div>
</template>

<script>
import Header from "./components/layout/Header";

export default {
  name: "app",
  components: {
    Header
  }
}
</script>
<style>
* {
  box-sizing: border-box;
  font-family:'Courier New', Courier, monospace;
  margin: 0;
  padding: 0;
}

:root {
  --black: #000000;
  --white: #ffffff;
  --grey: #3c3a3a;
  --lightGrey: #cccccc;
  --veryLightGrey: #f0ecec;
  --purple: #ca5ae6;
  --darkPurple: #743485;
}

.btn {
  display: inline-block;
  border: none;
  border-radius: 5rem;
  background: var(--black);
  color: var(--white);
  padding: 7px 20px;
  cursor: pointer;
}

.btn:hover {
  background: var(--grey);
}

</style>
