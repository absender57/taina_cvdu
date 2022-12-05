<script setup lang="ts">
console.log("test");
</script>

<template>
  <p>線形表示を行う</p>
  <div class="contents">
    <span>station name</span>
    <span>画面切替ボタン</span>
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
  p {
    margin: 5px;
    color: #42b983;
    font-size: 80px;
    border: dashed;
    height: 1.2em;
  }
  span {
    border: #42b983 solid;
    color: #42b983;
    margin: 5px;
    display: inline-block;
  }
}

.tool_bar {
  position: relative;
}

.route_setting {
  position: absolute;
  border: #42b983 solid 2px;
}

.point_setting {
  position: absolute;
  border: #42b983 solid 2px;
}

.non_visible {
  display: none;
}
</style>
