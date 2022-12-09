<script setup lang="ts">
console.log("test");
</script>

<template>
  <div class="contents">
    <span class="direction">方位</span>
    <span class="use1">計軸1</span>
    <span class="use_both">同時</span>
    <span class="use2">計軸2</span>
    <span class="failiure1">計軸1故障</span>
    <span class="failiure2">計軸２故障</span>
    <a class="reset1">計軸2リセット</a>
    <a class="reset2">計軸2リセット</a>
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
  grid-template-columns: repeat(4, auto);
  grid-template-rows: repeat(４, auto);
  place-items: center;

  span,
  button {
    border: solid;
    border-radius: 30%;
  }
  .direction {
    grid-column: 1 / 5;
    grid-row: 1;
  }

  .use1 {
    grid-column: 1;
    grid-row: 2;
  }

  .use_both {
    grid-column: 2 / 4;
    grid-row: 2;
  }

  .use2 {
    grid-column: 4;
    grid-row: 2;
  }

  .failiure1 {
    grid-column: 1 / 3;
    grid-row: 3;
  }

  .failiure2 {
    grid-column: 3 / 5;
    grid-row: 3;
  }

  .reset1 {
    grid-column: 1 / 3;
    grid-row: 4;
  }

  .reset2 {
    grid-column: 3 / 5;
    grid-row: 4;
  }
}
</style>
