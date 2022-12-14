<script setup lang="ts">
import axle_Counters from "./axle_counters.vue";
import station_Name from "./station_name.vue";
import failiure_status from "./fail_status.vue";
console.log("test");
</script>

<template>
  <div class="contents">
    <axle_Counters />
    <station_Name />
    <failiure_status />
    <span>画面反転</span>
    <div>
      <span>システム状態プルダウンウィンドウ</span>
      <div>
        <span>LOCAL</span>
        <span>CTC</span>
      </div>
      <div>
        <span>CVDU1</span>
        <span>CVDU2</span>
      </div>
      <span>電源故障ボタン</span>
      <span>連動故障ボタン</span>
      <span>転轍器故障ボタン</span>
      <span>断灯故障ボタン</span>
      <div>
        <span>A区保養</span>
        <button>應用</button>
        <button>取消</button>
      </div>
      <div>
        <span>NE封鎖</span>
        <button>控制</button>
        <button>取消</button>
      </div>
      <span>調車ボタン</span>
      <span>取り消しボタン</span>
      <span>進行定位確認及び取り消しボタン</span>
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
  border: solid;

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
