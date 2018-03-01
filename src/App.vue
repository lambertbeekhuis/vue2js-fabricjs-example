<template>
  <div id="app">
    <img width="25%" src="./assets/logo.png">
   
    <FabricVue/>
  </div>
</template>

<script>
import FabricVue from "./components/FabricVue";

export default {
  name: "App",
  components: {
    FabricVue
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
  margin-top: 60px;
}
</style>
