<script setup lang="ts">
import tool_bar from "./tool_bar.vue";
import route_setting from "./route_setting.vue";
import point_setting from "./point_setting.vue";
import { ref } from "vue";

const count: string = ref(0);
</script>

<template>
  <tool_bar class="tool_bar" />
  <route_setting class="route_setting" />
  <point_setting class="point_setting" />
  <p>線形画面を表示{{ count }}</p>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
p {
  margin: 5px;
  color: #42b983;
  font-size: 80px;
  border: dashed;
  height: 80vh;
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
  left: 100px;
}
</style>
