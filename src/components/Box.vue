<template>
  <div
    class="box"
    v-bind:style="{
    'background-color' : color, 
    'color': textColor,
    }"
  >{{text}}</div>
</template>

<script>
export default {
  name: "Box",
  props: {
    text: String,
    color: String,
    textColor: String
  },
  data() {},
  methods: {}
};
</script>

<style scoped>
.box {
  outline: 4px solid grey;
  text-align: center;
}
</style>
