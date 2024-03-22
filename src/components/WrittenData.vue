<script setup lang="ts">
import chartData from "../json/chartData.json"

</script>

<template>
  <div v-for="data in chartData.writtenData" class="data">
    <h5 class="title">{{data.name}}</h5>
    <h1 class="number">{{data.data}}</h1>
  </div>
</template>

<style scoped lang="scss">

.data{
  margin: 30px;
}

.title{
  color: #b0b0b0;
  margin: 0;
}

.number{
  font-size: 3rem;
  margin: 0;
  padding: 0;
}

</style>