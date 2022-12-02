<script setup lang="ts">
const number = 100;
const numbers = [...Array(number)].map((val, idx) => idx);
console.log(numbers);
</script>

<template>
  <div>
    <p>route setting</p>
    <ul class="container">
      <li v-for="n in numbers" :key="n">route{{ n }}</li>
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
  color: chartreuse;
}

li {
  padding: 2px 0;
  flex: 1;
  border: dashed rgb(61, 95, 10) 1px;
}
</style>
