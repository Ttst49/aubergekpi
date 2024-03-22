<template>

  <Doughnut />

</template>

<script setup lang="ts">
import { Doughnut } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'
ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)
import chartData from '../json/chartData.json'

const data = {
  value: chartData.gaugeData.totalUsers,
  max: 100000000,
  label: "Users"
};
export default {
  name: 'DoughnutChart',
  components: { Doughnut },
  data() {
    return {
      chartData: {
        labels: [data.label],
        datasets: [ {
          data: [data.value, data.max - data.value],
          backgroundColor: ['rgba(54, 162, 235, 0.8)', 'rgba(0, 0, 0, 0.1)'],
          borderWidth: 0
        } ]
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false,
        cutoutPercentage: 85,
        rotation: -90,
        circumference: 180,
        tooltips: {
          enabled: false
        },
        legend: {
          display: false
        },
        animation: {
          animateRotate: true,
          animateScale: false
        },
        title: {
          display: true,
          text: data.label,
          fontSize: 16
        }
      }
    };
  }
}

</script>


<style scoped lang="scss">

</style>