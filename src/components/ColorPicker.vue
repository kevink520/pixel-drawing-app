<template>
  <div>
    <Pixel isInColorPicker color="white" :current="color === 'white'" />
    <Pixel isInColorPicker color="lightblue" :current="color === 'lightblue'" />
    <Pixel isInColorPicker color="blue" :current="color === 'blue'" />
    <Pixel isInColorPicker color="darkblue" :current="color === 'darkblue'" />
  </div>
</template>

<script>
import Pixel from './Pixel';

export default {
  name: 'ColorPicker',
  props: {
    color: String
  },
  components: {
    Pixel
  }
}
</script>
