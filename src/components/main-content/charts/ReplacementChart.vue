<script setup>
import { ref } from 'vue'

const series = ref([
  {
    name: '<2022',
    data: [44, 55, 41, 67, 22, 43, 90]
  },
  {
    name: '2022',
    data: [13, 23, 20, 8, 13, 27, 34]
  },
  {
    name: '2023',
    data: [13, 23, 20, 8, 13, 27, 34]
  },
  {
    name: '2024',
    data: [11, 17, 15, 15, 21, 14, 65]
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
      columnWidth: '60%',
      // columnGap: '10%',
      barHeight: '100%',
      borderRadius: 5,
      borderRadiusApplication: 'around',
      borderRadiusWhenStacked: 'all'
    }
  },
  xaxis: {
    type: 'category',
    categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul']
  },
  legend: {
    show: false
  },
  fill: {
    opacity: 1
  },
  colors: ['#ADD8E6', '#1E90FF', '#FF6347', '#32CD32'],
  tooltip: {
    shared: true,
    intersect: false,
    y: {
      formatter: function (val) {
        return val
      }
    }
  }
})
</script>

<template>
  <div>
    <apexchart
      width="1000px"
      height="400px"
      type="bar"
      :options="chartOptions"
      :series="series"
    ></apexchart>
  </div>
</template>
