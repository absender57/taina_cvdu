<script setup lang="ts">
import "normalize.css";
import cvdu_main from "./components/cvdu_main.vue";
</script>

<template>
  <cvdu_main />
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  --main-bgColor: rgb(39, 39, 39);
  --main-shapeColor: rgb(66, 185, 131);
  background-color: var(--main-bgColor);
}
</style>
