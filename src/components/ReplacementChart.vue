<script setup>
import { ref } from 'vue'

const series = ref([
  {
    name: 'Product A',
    data: [44, 55, 41, 67, 22, 43, 21, 49, 62]
  },
  {
    name: 'Product B',
    data: [13, 23, 20, 8, 13, 27, 33, 12, 10]
  },
  {
    name: 'Product C',
    data: [11, 17, 15, 15, 21, 14, 13, 23, 20]
  }
])

const chartOptions = ref({
  chart: {
    type: 'bar',
    height: 350,
    stacked: true,
    zoom: {
      enabled: true
    }
  },
  responsive: [
    {
      breakpoint: 480,
      options: {
        legend: {
          position: 'bottom',
          offsetX: -10,
          offsetY: 0
        }
      }
    }
  ],
  plotOptions: {
    bar: {
      horizontal: false
    }
  },
  xaxis: {
    type: 'category',
    categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep']
  },
  legend: {
    position: 'right',
    offsetY: 40
  },
  fill: {
    opacity: 1
  }
})
</script>

<template>
  <div>
    <apexchart type="bar" :options="chartOptions" :series="series"></apexchart>
  </div>
</template>
