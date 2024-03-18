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

ChartJS.register(ArcElement,Title, Tooltip, Legend, CategoryScale, LinearScale)

export default {
  name: 'PieChart',
  components: { Pie },
  data() {
    return {
      chartData: {
        labels: [ 'Mer', 'Montagne', 'Tropical' ],
        datasets: [
            {
              data: [40, 20, 12],
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
