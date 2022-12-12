<script setup lang="ts">
import station_Name from "./station_name.vue";
import axle_Counters from "./axle_counters.vue";
console.log("test");
</script>

<template>
  <div class="contents">
    <station_Name />
    <span>画面反転</span>
    <axle_Counters />
    <div>
      <span>列車検知</span>
      <span>現在故障状態プルダウンウィンドウ</span>
      <span>システム状態プルダウンウィンドウ</span>
      <span>ローカルCTC切替ボタン</span>
      <span>cvdu1系、2系切替ボタン</span>
      <span>電源故障ボタン</span>
      <span>連動故障ボタン</span>
      <span>転轍器故障ボタン</span>
      <span>断灯故障ボタン</span>
      <span>保養ボタン</span>
      <span>封鎖ボタン</span>
      <span>調車ボタン</span>
      <span>取り消しボタン</span>
      <span>進行定位確認及び取り消しボタン</span>
      <span></span>
    </div>
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

  span {
    border: var(--main-shapeColor) solid;
    color: var(--main-shapeColor);
    margin: 5px;
    display: inline-block;
  }
}

.tool_bar {
  position: relative;
}

.route_setting {
  position: absolute;
  border: var(--main-shapeColor) solid 2px;
}

.point_setting {
  position: absolute;
  border: var(--main-shapeColor) solid 2px;
}

.non_visible {
  display: none;
}
</style>
