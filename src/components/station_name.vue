<script setup lang="ts">
console.log("stationName");
</script>

<template>
  <div class="contents">
    <p class="tradditionalChar">台南</p>
    <p class="alphabetChar">tai-nan</p>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.main {
  height: 90vh;
}

.contents {
  margin: 5px;
  color: var(--main-shapeColor);
  border: dashed;
  width: fit-content;
  display: grid;
  place-items: center;
  p {
    color: var(--main-shapeColor);
    margin: 5px;
    width: fit-content;
  }
  .tradditionalChar {
    font-size: 40px;
  }
  .alphabetChar {
    font-size: 20px;
  }
}
</style>
