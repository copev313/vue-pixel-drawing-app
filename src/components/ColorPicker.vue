<template>
  <div>
    <Pixel color="white"/>
    <Pixel color="lightblue"/>
    <Pixel color="blue"/>
    <Pixel color="darkblue"/>
  </div>
</template>

<script>
import Pixel from "./Pixel";

export default {
  name: "ColorPicker",
  components: {
    Pixel
  }
};
</script>

<style scoped>
</style>
