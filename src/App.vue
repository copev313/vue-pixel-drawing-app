<template>
  <div id="app">
    <ColorPicker :color="color"/>
    <Canvas/>
  </div>
</template>

<script>
import Canvas from "./components/Canvas";
import ColorPicker from "./components/ColorPicker";

export default {
  name: "App",
  data: function() {
    return {
      color: "white"
    };
  },
  components: {
    Canvas,
    ColorPicker
  },
  mounted() {
    this.$root.$on("updatecolor", color => {
      this.color = color;
    });
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #333;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
</style>
