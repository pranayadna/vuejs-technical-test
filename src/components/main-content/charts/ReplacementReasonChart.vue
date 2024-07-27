<script setup>
import { ref } from 'vue'

const series = ref([
  {
    name: 'Rusak',
    data: [44, 55, 41, 67, 22, 43]
  },
  {
    name: 'Hilang',
    data: [13, 23, 20, 8, 13, 27]
  },
  {
    name: 'Lain-Lain',
    data: [11, 17, 15, 15, 21, 14]
  }
])

const chartOptions = ref({
  dataLabels: {
    enabled: false
  },
  chart: {
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
      horizontal: false,
      columnWidth: '30%',
      barHeight: '100%',
      borderRadius: 5,
      borderRadiusApplication: 'around',
      borderRadiusWhenStacked: 'all'
    }
  },
  xaxis: {
    type: 'category',
    categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun']
  },
  legend: {
    show: 'false'
  },
  fill: {
    opacity: 1
  },
  colors: ['#1E90FF', '#32CD32', '#FF6347']
})
</script>

<template>
  <div>
    <apexchart height="250" type="bar" :options="chartOptions" :series="series"></apexchart>
  </div>
</template>
