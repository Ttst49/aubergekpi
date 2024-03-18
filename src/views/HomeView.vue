<template>
  <Pie />
  <LineChart />
  <WrittenData msg="Auberges actives" number-data="12 834"/>
  <WrittenData msg="Utilisateurs actifs" number-data="8 027 809"/>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Pie from '@/components/Pie.vue';
import LineChart from "@/components/LineChart.vue";
import WrittenData from "@/components/WrittenData.vue";
@Options({
  components: {
    WrittenData,
    Pie,
    LineChart
  },
})
export default class HomeView extends Vue {}
</script>
