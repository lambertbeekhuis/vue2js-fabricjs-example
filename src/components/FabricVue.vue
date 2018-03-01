<template>
  <div id="fabriccanvas">
  {{msg}}
  
  <canvas id="c"></canvas>
  <button v-on:click="addObject" class="btn btn-primary">Add</button>


   {{msg2}}
  </div>
</template>

<script>
import { fabric } from "fabric/dist/fabric.js";

export default {
  name: "FabricVue",

  data() {
    return {
      msg: "Integrate fabricjs with Vue2.js",
      msg2: "End"
    };
  },

  methods: {
    addObject: function() {
      // create a rectangle object
      alert("Add a box");

      var rect2 = new fabric.Rect({
        left: 50,
        top: 50,
        fill: "green",
        width: 40,
        height: 20
      });

      this.canvas.add(rect2);
    }
  },

  mounted: function() {
    var canvas = new fabric.Canvas("c", {
      backgroundColor: "greenyellow"
    });

    this.canvas = canvas;

    // create a rectangle object
    var rect = new fabric.Rect({
      left: 100,
      top: 100,
      fill: "red",
      width: 40,
      height: 20
    });

    // "add" rectangle onto canvas
    canvas.add(rect);
  }
};
</script>

<style>

</style>
