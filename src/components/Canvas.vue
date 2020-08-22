<template>
  <div class="canvas">
    <Pixel isInCanvas v-for="(color, index) in pixels" :key="index" :index="index" :color="color"/>
  </div>
</template>

<script>
import Pixel from "./Pixel";

export default {
  name: "Canvas",
  components: {
    Pixel
  },
  props: {
    pixels: Array
  }
};
</script>

<style scoped>
.canvas {
  display: flex;
  flex-wrap: wrap;
  max-width: 900px;
}
</style>
