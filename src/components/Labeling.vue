<template>
  <div style="height: 800px; width: 1000px; border: 1px solid red; position: relative;">
    <vue-draggable-resizable style="border:5px solid" @click.native="clicked"  :w="100" :h="100" @dragging="onDrag" @resizing="onResize" :parent="true">
      <p>X: {{ x }} / Y: {{ y }} - W: {{ width }} / H: {{ height }}</p>
    </vue-draggable-resizable>
  </div>
</template>

<script>
//import VueDraggableResizable from 'vue-draggable-resizable'

export default {
  data: function () {
    return {
      width: 0,
      height: 0,
      x: 0,
      y: 0
    }
  },
  methods: {
    clicked: function(){
        console.log("clicked")
    },
    onResize: function (x, y, width, height) {
      this.x = x
      this.y = y
      this.width = width
      this.height = height
    },
    onDrag: function (x, y) {
      this.x = x
      this.y = y
    }
  }
}
</script>