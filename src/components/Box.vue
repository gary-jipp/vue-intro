<template>
  <div
    class="box"
    @mouseover="mouseOver"
    @mouseleave="mouseOver"
    :style="{
    'background-color' : hover? hoverColor : color, 
    'color': textColor,
    }"
  >
  {{text}}
    <slot />
  </div>
</template>

<script>
export default {
  name: "Box",
  props: {
    text: String,
    color: { type: String, default: "grey" },
    textColor: { type: String, default: "white" },
    hoverColor: { type: String, default: "lightGrey" }
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
