<script setup>
import { ref } from 'vue'

const series = ref([
  {
    name: 'Sales',
    data: [10, 41, 35, 51, 49, 62]
  }
])

const chartOptions = ref({
  chart: {
    type: 'line',
    height: 350,
    zoom: {
      enabled: false
    }
  },
  dataLabels: {
    enabled: false
  },
  stroke: {
    curve: 'smooth'
  },
  grid: {
    row: {
      colors: ['#f3f3f3', 'transparent'],
      opacity: 0.5
    }
  },
  xaxis: {
    categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun']
  }
})
</script>

<template>
  <div>
    <apexchart height="250" type="line" :options="chartOptions" :series="series"></apexchart>
  </div>
</template>
