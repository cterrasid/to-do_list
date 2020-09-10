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
}

</style>
