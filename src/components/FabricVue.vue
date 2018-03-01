<template>
  <div id="fabriccanvas">
  {{msg}}
  
  <canvas id="c"></canvas>

  <button v-on:click="addObject" class="btn btn-primary">Add a box</button>

  <button v-on:click="saveToJson" class="btn btn-primary">Save to JSON</button>

  <div>{{json}}</div>


<div>
   {{msg2}}
   </div>
  </div>
</template>

<script>
import { fabric } from "fabric/dist/fabric.js";

export default {
  name: "FabricVue",

  data() {
    return {
      msg: "Integrate fabricjs with Vue2.js",
      msg2: "End",
      json: ""
    };
  },

  methods: {
    addObject: function() {
      // create a rectangle object

      var rect2 = new fabric.Rect({
        left: 50,
        top: 50,
        fill: "green",
        width: 40,
        height: 20
      });

      this.canvas.add(rect2);
    },

    saveToJson: function() {
      this.json = JSON.stringify(this.canvas);
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
