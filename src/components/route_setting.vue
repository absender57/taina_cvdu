<script setup lang="ts">
const number = 100;
const numbers = [...Array(number)].map((val, idx) => idx);
console.log(numbers);
</script>

<template>
  <ul class="container">
    <li v-for="n in numbers" :key="n">route{{ n }}</li>
  </ul>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container {
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  background-color: rgb(239, 239, 239);
  padding: 2px;
  width: 50%;
}

li {
  margin-right: 10px;
  flex: 1;
}
</style>
