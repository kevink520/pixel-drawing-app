<template>
  <div class="canvas">
    <Pixel isInCanvas v-for="(color, index) in pixels" :key="index" :index="index" :color="color" />
  </div>
</template>

<script>
  import Pixel from './Pixel';

  export default {
    name: 'Canvas',
    components: {
      Pixel
    },
    props: {
      pixels: Array,
      color: String
    },
    mounted() {
      this.$root.$on('clickedpixel', index => {
        this.pixels.splice(index, 1, this.color);
      });
    }
  }
</script>

<style>
  .canvas {
    display: flex;
    flex-wrap: wrap;
    max-width: 900px;
  }
</style>
