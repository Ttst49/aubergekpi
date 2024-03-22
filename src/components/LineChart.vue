<template>
  <Line
      id="my-chart-id"
      :options="chartOptions"
      :data="chartData"
  />
</template>

<script>
import { Line } from 'vue-chartjs'
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  CategoryScale,
  LinearScale,
  LineElement,
  PointElement,
    Filler
} from 'chart.js'
import chartData from "@/json/chartData.json";

ChartJS.register(LineElement,Title, Tooltip, Legend, CategoryScale, LinearScale,PointElement,Filler)

let years = []
let values = []
for (let i=0; i < chartData.lineData.usersPerYear.length; i++) {
  years.push(chartData.lineData.usersPerYear[i].year)
  values.push(chartData.lineData.usersPerYear[i].value)
}


export default {
  name: 'PieChart',
  components: { Line },
  data() {
    return {
      chartData: {
        labels: years,
        datasets: [
          {
            label:"All users by year",
            data: values,
            fill: false,
            borderColor: 'rgb(38,101,220)',
            tension: 0,
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
