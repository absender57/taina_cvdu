<script setup lang="ts">
const number = 100;
const numbers = [...Array(number)].map((val, idx) => idx);
console.log(numbers);
</script>

<template>
  <div>
    <p>point control</p>
    <ul class="container">
      <li v-for="n in numbers" :key="n">point{{ n }}</li>
    </ul>
  </div>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container {
  list-style: none;
  display: grid;
  grid-template-columns: repeat(7, 80px);
  flex-wrap: wrap;
  flex-direction: row;
  background-color: rgb(239, 239, 239);
  padding: 2px;
}

P {
  width: auto;
  color: var(--main-shapeColor);
  background-color: rgb(239, 239, 239);
  margin: 0;
}

ul {
  margin: 0;
}

li {
  padding: 2px 0;
  flex: 1;
  color: var(--main-shapeColor);
  border: dashed rgb(61, 95, 10) 1px;
}
</style>
