<template>
  <div @click="handleClick" :class="['pixel', color, current ? 'current' : '']"></div>
</template>

<script>
export default {
  name: 'Pixel',
  props: {
    color: String,
    current: Boolean,
    isInColorPicker: Boolean,
    isInCanvas: Boolean,
    index: Number
  },
  methods: {
    handleClick() {
      if (this.isInColorPicker) {
        this.$root.$emit('updatecolor', this.color);
      }

      if (this.isInCanvas) {
        this.$root.$emit('clickedpixel', this.index);
      }
    }
  }
};
</script>

<style scoped>
  .pixel {
    border: 1px solid lightgray;
    width: 30px;
    height: 30px;
    box-sizing: border-box;
  }
  .white {
    background-color: white;
  }
  .lightred {
    background-color: #e57373;
  }
  .red {
    background-color: #ff0900;
  }
  .darkred {
    background-color: #b71c1c;
  }
  .lightorange {
    background-color: #ffb74d;
  }
  .orange {
    background-color: #ff7f00;
  }
  .darkorange {
    background-color: #e65100;
  }
  .lightyellow {
    background-color: #fff59d;
  }
  .yellow {
    background-color: #ffef00;
  }
  .darkyellow {
    background-color: #fbc02d;
  }
  .lightgreen {
    background-color: #81c784;
  }
  .green {
    background-color: #00f11d;
  }
  .darkgreen {
    background-color: #1b5e20;
  }
  .lightblue {
    background-color: #64b5f6;
  }
  .blue {
    background-color: #0079ff;
  }
  .darkblue {
    background-color: #0d47a1;
  }
  .lightindigo {
    background-color: #7986cb;
  }
  .indigo {
    background-color: #3949ab;
  }
  .darkindigo {
    background-color: #1a237e;
  }
  .lightpurple {
    background-color: #9575cd;
  }
  .purple {
    background-color: #a800ff;
  }
  .darkpurple {
    background-color: #311b92;
  }
  .current {
    border: 4px solid yellow;
  }
</style>
