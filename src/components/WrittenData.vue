<script setup lang="ts">

defineProps(['msg','numberData'])

</script>

<template>
  <div class="data">
    <h5 class="title">{{msg}}</h5>
    <h1 class="number">{{numberData}}</h1>
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