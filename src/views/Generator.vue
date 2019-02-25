<script>
import SvgCanvas from '../components/SvgCanvas'

export default {
  components: {
    SvgCanvas
  },
  data() {
    return {
      elements: [],
      rectWidth: 0
    }
  },
  methods: {
    addRectangle() {
      this.elements.push(
        {
          tag: 'rect',
          attrs: {
            width: 50,
            height: 50,
            x: 10,
            y: 20
          }
        }
      )
    }
  }
}
</script>

<template>
	<div>
    <svg-canvas :elements="elements"></svg-canvas>
    <div class="palette">
      <button @click="addRectangle">Add Rectangle</button>
    </div>
  </div>
</template>

<style lang="scss">
svg {
  border: 1px solid red;
}
</style>
