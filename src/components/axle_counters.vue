<script setup lang="ts">
import { ref } from "vue";
import axle_Counter from "./axle_counter.vue";
const directions = ref([
  {
    title: "NE",
    useState: {
      axle1: true,
      axle2: false,
      both: false,
    },
    failiureState: {
      axle1: true,
      axle2: false,
    },
  },
  {
    title: "NW",
    useState: {
      axle1: false,
      axle2: true,
      both: false,
    },
    failiureState: {
      axle1: true,
      axle2: false,
    },
  },
  {
    title: "M",
    useState: {
      axle1: true,
      axle2: false,
      both: false,
    },
    failiureState: {
      axle1: true,
      axle2: false,
    },
  },
  {
    title: "SE",
    useState: {
      axle1: true,
      axle2: false,
      both: false,
    },
    failiureState: {
      axle1: false,
      axle2: false,
    },
  },
  {
    title: "SW",
    useState: {
      axle1: true,
      axle2: false,
      both: false,
    },
    failiureState: {
      axle1: false,
      axle2: true,
    },
  },
]);
</script>

<template>
  <div class="axleCounters">
    <axle_Counter
      v-for="direction in directions"
      :key="direction.title"
      v-bind:direction="direction"
    />
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.axleCounters {
  margin: 5px;
  color: var(--main-shapeColor);
  border-right: solid var(--main-shapeColor);
  width: fit-content;
  display: grid;
  grid-template-columns: repeat(5, auto);
  grid-template-rows: repeat(5, auto);
  place-items: center;
}
</style>
