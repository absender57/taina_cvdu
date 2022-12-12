<script setup lang="ts">
import { FLATTENABLE_KEYS } from "@babel/types";
import { ref } from "vue";
import axle_Counter from "./axle_counter.vue";
const directions = [
  { title: "NE", useState: { axle1: true } },
  { title: "NW", useState: { axle1: true } },
  { title: "M", useState: { axle1: true } },
  { title: "SE", useState: { axle1: true } },
  { title: "SW", useState: { axle1: true } },
];
</script>

<template>
  <div class="contents">
    <axle_Counter
      v-for="direction in directions"
      :key="direction.title"
      v-bind:direction="direction"
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
