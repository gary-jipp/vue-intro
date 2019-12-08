<template>
  <div
    class="box"
    @mouseover="mouseOver"
    v-on:mouseleave="mouseOver"
    v-bind:style="{
    'background-color' : hover? hoverColor : color, 
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
    textColor: String,
    hoverColor: { type: String, default: "grey" }
  },
  data() {
    return {
      hover: false
    };
  },
  methods: {
    mouseOver() {
      this.hover = !this.hover;
    }
  }
};
</script>

<style scoped>
.box {
  outline: 4px solid grey;
  text-align: center;
}
</style>
