<script setup>
import { ref } from 'vue'

const series = ref([44, 55, 13, 43, 22])

const chartOptions = ref({
  chart: {
    type: 'pie',
    height: 350
  },
  labels: ['Product A', 'Product B', 'Product C', 'Product D', 'Product E'],
  responsive: [
    {
      breakpoint: 480,
      options: {
        chart: {
          width: 200
        },
        legend: {
          position: 'bottom'
        }
      }
    }
  ]
})
</script>

<template>
  <div>
    <apexchart type="pie" :options="chartOptions" :series="series"></apexchart>
  </div>
</template>
