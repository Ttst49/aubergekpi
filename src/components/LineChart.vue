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

ChartJS.register(LineElement,Title, Tooltip, Legend, CategoryScale, LinearScale,PointElement,Filler)

export default {
  name: 'PieChart',
  components: { Line },
  data() {
    return {
      chartData: {
        labels: [ 'Mer', 'Montagne', 'Tropical',"banane","poire","peche","abricot","pomme","cerise","framboise","myrtille","litchi" ],
        datasets: [
          {
            data: [403, 220, 129,185,431,138,2337,273,1823,3672,822,743],
            fill: false,
            borderColor: 'rgb(82,248,103)',
            tension: 0
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
