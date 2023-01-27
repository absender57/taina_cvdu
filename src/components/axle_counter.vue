<script setup lang="ts">
import { defineProps } from "vue";
const props = defineProps<{
  direction: {
    title: string;
    useState: {
      axle1: boolean;
      axle2: boolean;
      both: boolean;
    };
    failiureState: {
      axle1: boolean;
      axle2: boolean;
    };
  };
}>();
</script>

<template>
  <div class="axleCounter">
    <span class="direction">{{ props.direction.title }}</span>
    <span class="axle1">計軸1</span>
    <span class="both">同時</span>
    <span class="axle2">計軸2</span>
    <span
      class="use1"
      :class="{
        yellow: props.direction.useState.axle1,
        red: !props.direction.useState.axle1,
      }"
    ></span>
    <span
      class="use_both"
      :class="{ green: props.direction.useState.both }"
    ></span>
    <span
      class="use2"
      :class="{
        yellow: props.direction.useState.axle2,
        red: !props.direction.useState.axle2,
      }"
    ></span>
    <span
      class="failiure1"
      :class="{ red: props.direction.failiureState.axle1 }"
    >
      故障
    </span>
    <span
      class="failiure2"
      :class="{ red: props.direction.failiureState.axle2 }"
    >
      故障
    </span>
    <button class="reset1">重置</button>
    <button class="reset2">重置</button>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.axleCounter {
  color: var(--main-shapeColor);
  border-top: solid var(--main-shapeColor);
  border-left: solid var(--main-shapeColor);
  border-bottom: solid var(--main-shapeColor);
  width: fit-content;
  display: grid;
  grid-template-columns: repeat(2, auto) 50px repeat(2, auto);
  grid-template-rows: repeat(5, auto);
  place-items: center;

  span,
  button {
    border: solid var(--main-shapeColor);
    margin: 2px;
  }

  .direction {
    grid-column: 1 / 6;
    grid-row: 1;
    border: 0ch;
  }

  .axle1 {
    grid-column: 1 / 3;
    grid-row: 2;
    border: 0ch;
  }

  .both {
    grid-column: 3;
    grid-row: 2;
    border: 0ch;
  }

  .axle2 {
    grid-column: 4 / 6;
    grid-row: 2;
    border: 0ch;
  }

  .use1 {
    grid-column: 1 / 3;
    grid-row: 3;
    width: 20px;
    height: 20px;
    border-radius: 50%;
  }

  .use_both {
    grid-column: 3;
    grid-row: 3;
    width: 20px;
    height: 20px;
    border-radius: 50%;
  }

  .use2 {
    grid-column: 4 / 6;
    grid-row: 3;
    width: 20px;
    height: 20px;
    border-radius: 50%;
  }

  .failiure1 {
    grid-column: 1 / 3;
    grid-row: 4;
    border-radius: 10% / 50%;
    padding: 0px 5px;
  }

  .failiure2 {
    grid-column: 4 / 6;
    grid-row: 4;
    border-radius: 10% / 50%;
    padding: 0px 5px;
  }

  .reset1 {
    grid-column: 1 / 3;
    grid-row: 5;
    background-color: var(--main-bgcolor);
    color: var(--main-shapeColor);
    cursor: pointer;
  }

  .reset2 {
    grid-column: 4 / 6;
    grid-row: 5;
    background-color: var(--main-bgcolor);
    color: var(--main-shapeColor);
    cursor: pointer;
  }

  .red {
    color: white;
    background-color: red;
  }

  .yellow {
    background-color: yellow;
  }

  .green {
    background-color: green;
  }
}
</style>
