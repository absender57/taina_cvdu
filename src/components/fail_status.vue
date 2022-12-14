<script setup lang="ts">
import { ref } from "vue";
const lowBatterryNorth = ref(true);
const lowBatterryStation = ref(false);
const lowBatterrySouth = ref(false);
const lowBatterry = ref(
  lowBatterryNorth.value || lowBatterryStation.value || lowBatterrySouth.value
);
</script>

<template>
  <div class="failiureContainer">
    <details>
      <summary :class="{ red: lowBatterry }">低電圧</summary>
      <ul>
        <li :class="{ red: lowBatterryNorth }">北中途</li>
        <li :class="{ red: lowBatterryStation }">站内</li>
        <li :class="{ red: lowBatterrySouth }">南中途</li>
      </ul>
    </details>

    <span>発電機</span>

    <details>
      <summary>転轍機</summary>
      <ul>
        <li>11</li>
        <li>13</li>
        <li>14</li>
      </ul>
    </details>

    <details>
      <summary>断灯</summary>
      <ul>
        <li>1LA</li>
        <li>1LB</li>
        <li>2RA</li>
        <li>4RA</li>
      </ul>
    </details>

    <details>
      <summary>接地</summary>
      <ul>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </details>

    <details>
      <summary>断電</summary>
      <ul>
        <li>北中途断電</li>
        <li>站内談電</li>
        <li>南中途断電</li>
      </ul>
    </details>

    <details>
      <summary>連動故障</summary>
      <ul>
        <li>IE</li>
        <li>NIF</li>
        <li>FOC</li>
        <li>FS-PCL</li>
      </ul>
    </details>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.failiureContainer {
  margin: 5px;
  color: var(--main-shapeColor);
  width: fit-content;
  display: grid;
  place-items: start;
  text-align: start;

  summary {
    place-content: start;
    place-items: start;
  }

  ul {
    margin: 0%;
  }
  .red {
    border-bottom: solid red 2px;
  }
}
</style>
