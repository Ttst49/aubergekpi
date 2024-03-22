<template>
  <Pie
      id="my-chart-id"
      :options="chartOptions"
      :data="chartData"
  />
</template>

<script>
import { Pie } from 'vue-chartjs'
import {Chart as ChartJS, Title, Tooltip, Legend, CategoryScale, LinearScale, ArcElement} from 'chart.js'
import chartData from "../json/chartData.json"
import {data} from "autoprefixer";

ChartJS.register(ArcElement,Title, Tooltip, Legend, CategoryScale, LinearScale)
let labels = []
let values = []
for (let i=0; i < chartData.pieData.length; i++) {
  labels.push(chartData.pieData[i].name)
  values.push(chartData.pieData[i].value)
}


export default {
  name: 'PieChart',
  components: { Pie },
  data() {

    return {
      chartData: {
        labels: labels,
        datasets: [
            {
              data: values,
              backgroundColor: [
                '#0072F0',
                '#2E8BF3',
                '#5CA5F5'
              ]
            }
        ],
      },
      chartOptions: {
        responsive: false
      }
    }
  }
}

</script>
