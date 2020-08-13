<template>
  <div>
    <Pixel isInColorPicker color="white" :current="color === 'white'" />
    <Pixel isInColorPicker color="lightred" :current="color === 'lightred'" />
    <Pixel isInColorPicker color="red" :current="color === 'red'" />
    <Pixel isInColorPicker color="darkred" :current="color === 'darkred'" />
    <Pixel isInColorPicker color="lightorange" :current="color === 'lightorange'" />
    <Pixel isInColorPicker color="orange" :current="color === 'orange'" />
    <Pixel isInColorPicker color="darkorange" :current="color === 'darkorange'" />
    <Pixel isInColorPicker color="lightyellow" :current="color === 'lightyellow'" />
    <Pixel isInColorPicker color="yellow" :current="color === 'yellow'" />
    <Pixel isInColorPicker color="darkyellow" :current="color === 'darkyellow'" />
    <Pixel isInColorPicker color="lightgreen" :current="color === 'lightgreen'" />
    <Pixel isInColorPicker color="green" :current="color === 'green'" />
    <Pixel isInColorPicker color="darkgreen" :current="color === 'darkgreen'" />
    <Pixel isInColorPicker color="lightblue" :current="color === 'lightblue'" />
    <Pixel isInColorPicker color="blue" :current="color === 'blue'" />
    <Pixel isInColorPicker color="darkblue" :current="color === 'darkblue'" />
    <Pixel isInColorPicker color="lightindigo" :current="color === 'lightindigo'" />
    <Pixel isInColorPicker color="indigo" :current="color === 'indigo'" />
    <Pixel isInColorPicker color="darkindigo" :current="color === 'darkindigo'" />
    <Pixel isInColorPicker color="lightpurple" :current="color === 'lightpurple'" />
    <Pixel isInColorPicker color="purple" :current="color === 'purple'" />
    <Pixel isInColorPicker color="darkpurple" :current="color === 'darkpurple'" />
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
