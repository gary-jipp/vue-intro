<template>
  <div id="app">
    <Box v-for="item of boxData" :text="item.text" v-bind="boxColor" :key="item.id">
      <!-- content ends up in Box slot -->
      {{item.id}}
    </Box>
  </div>
</template>

<script>
import Box from "./components/Box.vue";
export default {
  name: "app",
  components: {
    Box
  },
  data: function() {
    return {
      boxColor: { color: "green", textColor: "white", hoverColor: "Peru" },
      boxData: [
        { id: 1, text: "Box" },
        { id: 2, text: "Box" },
        { id: 3, text: "Box" },
        { id: 4, text: "Box" },
        { id: 5, text: "Box" },
        { id: 6, text: "Box" }
      ]
    };
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