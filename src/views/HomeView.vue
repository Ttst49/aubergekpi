<template>
  <Pie />
  <LineChart />

</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Pie from '@/components/Pie.vue';
import LineChart from "@/components/LineChart.vue";
@Options({
  components: {
    Pie,
    LineChart
  },
})
export default class HomeView extends Vue {}
</script>
