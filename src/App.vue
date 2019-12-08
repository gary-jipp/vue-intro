<template>
  <div id="app">
    <Box text="Box 1" color="green" textColor="white" />
    <Box text="Box 2" color="blue" textColor="white" />
    <Box text="Box 3" color="red" textColor="white" />
    <Box text="Box 4" color="red" textColor="white" />
    <Box text="Box 5" color="green" textColor="white" />
    <Box text="Box 6" color="blue" textColor="white" />
  </div>
</template>

<script>
import Box from "./components/Box.vue";

export default {
  name: "app",
  components: {
    Box
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 60px;
}

#app {
  display: grid;
  grid-template-columns: repeat(3, 200px);
  grid-template-rows: repeat(3, 100px);
  row-gap: 12px;
  column-gap: 12px;
}
</style>