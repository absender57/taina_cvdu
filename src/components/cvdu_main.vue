<script setup lang="ts">
import tool_bar from "./tool_bar.vue";
import route_setting from "./route_setting.vue";
import point_setting from "./point_setting.vue";
import line_view from "./line_view.vue";
import { ref } from "vue";
let routeSettingIsNonvible = ref(true);
let pointControlIsNonvible = ref(true);

const openedManu = (param: string) => {
  if (param == "routeSetting") {
    routeSettingIsNonvible.value = !routeSettingIsNonvible.value;
    pointControlIsNonvible.value = true;
  } else if (param == "pointControl") {
    routeSettingIsNonvible.value = true;
    pointControlIsNonvible.value = !pointControlIsNonvible.value;
  }
};
</script>

<template>
  <tool_bar class="tool_bar" @eventClick="openedManu" />
  <route_setting
    class="route_setting"
    :class="{ non_visible: routeSettingIsNonvible }"
  />
  <point_setting
    class="point_setting"
    :class="{ non_visible: pointControlIsNonvible }"
  />
  <line_view class="line_view" />
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.tool_bar {
  position: relative;
  height: 10vh;
}

.line_view {
  height: 90vh;
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
