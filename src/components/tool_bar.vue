<!-- <script setup lang="ts">
</script> -->

<template>
  <div class="container">
    <button class="manu" @click="$emit('eventClick', 'routeSetting')">
      Route Setting [F1]
    </button>
    <button class="manu" @click="$emit('eventClick', 'pointControl')">
      Point Control [F2]
    </button>
    <button class="manu">Event [F1]</button>
    <button class="manu">Others [F4]</button>
    <button class="manu">Failiure [F5]</button>
    <button class="manu">Maitenance [F6]</button>
    <div class="failiureHistory">
      <p>2022/12/01 11:00 hogehoge</p>
      <p>2022/12/01 11:00 hogehoge</p>
      <p>2022/12/01 11:00 hogehoge</p>
      <p>2022/12/01 11:00 hogehoge</p>
      <p>2022/12/01 11:00 hogehoge</p>
      <p>2022/12/01 11:00 hogehoge</p>
    </div>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container {
  display: flex;
  flex-direction: row;
  height: 100%;

  .manu {
    box-sizing: border-box;
    color: var(--main-shapeColor);
    border: solid var(--main-shapeColor) 2px;
    margin: 5px 5px;
    width: 70px;
    height: 70px;
    word-wrap: break-word;
    background-color: var(--main-bgColor);
  }

  .failiureHistory {
    box-sizing: border-box;
    color: var(--main-shapeColor);
    border: solid var(--main-shapeColor) 2px;
    margin: 5px 5px;
    width: 500px;
    height: 100%;
    text-align: left;
    padding: 5px;
    overflow-y: scroll;

    p {
      margin: 0%;
    }
  }

  :last-child {
    margin-left: auto;
  }
}
</style>
