<script setup lang="ts">
import axle_Counters from "./axle_counters.vue";
import station_Name from "./station_name.vue";
import failiure_status from "./fail_status.vue";
console.log("test");
</script>

<template>
  <div class="contents">
    <div class="upper">
      <axle_Counters />
      <station_Name />
      <failiure_status />
    </div>
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
        <span>表示</span>
        <button>控制</button>
        <button>取消</button>
      </div>
      <div>
        <span>NE封鎖</span>
        <span>表示</span>
        <button>控制</button>
        <button>取消</button>
      </div>
      <span>調車ボタン</span>
      <span>取り消しボタン</span>
      <span>進行定位確認及び取り消しボタン</span>
    </div>
    <div class="test">
      <span class="title"></span>
      <span class="title">計軸1</span>
      <span class="title">同時</span>
      <span class="title">計軸2</span>
      <span class="title">計軸1故障</span>
      <span class="title">計軸2故障</span>
      <span class="name">NE</span>
      <span class="usage1"></span>
      <span class="usageBoth"></span>
      <span class="usage2"></span>
      <span class="failiure1"></span>
      <span class="failiure2"></span>
      <span class="name">NW</span>
      <span class="usage1"></span>
      <span class="usageBoth"></span>
      <span class="usage2"></span>
      <span class="failiure1"></span>
      <span class="failiure2"></span>
      <span class="name">M</span>
      <span class="usage1"></span>
      <span class="usageBoth"></span>
      <span class="usage2"></span>
      <span class="failiure1"></span>
      <span class="failiure2"></span>
      <span class="name">SE</span>
      <span class="usage1"></span>
      <span class="usageBoth"></span>
      <span class="usage2"></span>
      <span class="failiure1"></span>
      <span class="failiure2"></span>
      <span class="name">SW</span>
      <span class="usage1"></span>
      <span class="usageBoth"></span>
      <span class="usage2"></span>
      <span class="failiure1"></span>
      <span class="failiure2"></span>
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

  .upper {
    display: flex;
    justify-content: space-between;
  }

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
.test {
  display: grid;
  grid-template-columns: repeat(6, minmax(30px, max-content));
  justify-items: center;
  span {
    border: solid 2px whitesmoke;
    border-radius: 5px;
    margin: 2px;
    margin-right: 5px;
  }
  .title {
    border: none;
  }
  .name {
    border: none;
  }
  .usage1 {
    width: 20px;
    height: 20px;
    background-color: yellow;
    color: rgb(46, 46, 46);
    border-radius: 50%;
  }
  .usageBoth {
    width: 20px;
    height: 20px;
    color: rgb(46, 46, 46);
    border-radius: 50%;
  }
  .usage2 {
    width: 20px;
    height: 20px;
    background-color: red;
    color: rgb(46, 46, 46);
    border-radius: 50%;
  }
  .failiure1 {
    width: 20px;
    height: 20px;
    color: rgb(46, 46, 46);
  }
  .failiure1:hover,
  .failiure2:hover {
    cursor: pointer;
  }
  .failiure2 {
    width: 20px;
    height: 20px;
    color: rgb(46, 46, 46);
  }
}
</style>
