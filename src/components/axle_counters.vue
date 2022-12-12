<script setup lang="ts">
import { FLATTENABLE_KEYS } from "@babel/types";
import axle_Counter from "./axle_counter.vue";

import { ref } from "vue";
console.log("test");
const directions = ref(["NE", "NW", "M", "SE", "SW"]);
</script>

<template>
  <div class="contents">
    <axle_Counter
      v-for="direction in directions"
      :key="direction"
      :directionName="direction"
    />
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.contents {
  margin: 5px;
  color: var(--main-shapeColor);
  border: dashed;
  width: fit-content;
  display: grid;
  grid-template-columns: repeat(5, auto);
  grid-template-rows: repeat(5, auto);
  place-items: center;
}
</style>
