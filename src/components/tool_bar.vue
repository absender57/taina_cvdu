<script setup lang="ts">
console.log("test");
</script>

<template>
  <div class="container">
    <button class="manu">Route Setting [F2]</button>
    <button class="manu">Point Control [F3]</button>
    <button class="manu">Row Data [F1]</button>
    <button class="manu">Others [F4]</button>
    <button class="manu" @click="openChildWindow">5</button>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container {
  display: flex;
  flex-direction: row;

  .manu {
    color: #42b983;
    border: solid #42b983 2px;
    margin: 0 5px;
    width: 70px;
    height: 70px;
  }
}
</style>
