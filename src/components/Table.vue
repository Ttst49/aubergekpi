<script setup lang="ts">
import chartData from "../json/chartData.json"

</script>

<template>


  <div class="relative overflow-x-auto">
    <table class="w-full text-sm text-left rtl:text-right text-gray-500 dark:text-gray-400">
      <thead class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
      <tr>
        <th scope="col" class="px-6 py-3">
          Country
        </th>
        <th scope="col" class="px-6 py-3">
          Users
        </th>
        <th scope="col" class="px-6 py-3">
          Device
        </th>
        <th scope="col" class="px-6 py-3">
          Impressions
        </th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="data in chartData.tableData" class="bg-white border-b dark:bg-gray-800 dark:border-gray-700">
        <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
          {{ data.country }}
        </th>
        <td class="px-6 py-4">
          {{ data.users }}
        </td>
        <td class="px-6 py-4">
          {{ data.device }}
        </td>
        <td class="px-6 py-4">
          {{ data.impressions }}
        </td>
      </tr>
      </tbody>
    </table>
  </div>

</template>

<style scoped lang="scss">

</style>