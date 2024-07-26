<script setup>
import { ref, computed } from 'vue'

// Define series with names and data
const series = ref([38, 15, 22, 25])
const labels = ['2024', '2023', '2022', 'Others']

// const combinedData = computed(() => {
//   return series.value.map((value, index) => {
//     return { label: labels[index], value: value }
//   })
// })

// Flatten series data for the chart
// const series = computed(() => seriesData.value.map((s) => s.data[0]))
const highestValue = computed(() => Math.max(...series.value))

const chartOptions = ref({
  dataLabels: {
    enabled: false
  },
  responsive: [
    {
      breakpoint: 480,
      options: {
        chart: {
          width: 100
        },
        legend: {
          show: false
        }
      }
    }
  ],
  labels: labels,
  legend: {
    position: 'bottom',
    offsetX: 0,
    offsetY: 14,
    fontSize: '20px',
    itemMargin: {
      horizontal: 69,
      vertical: 4
    },
    formatter: (seriesName, opts) => {
      const index = opts.seriesIndex
      const value = series.value[index]
      return `${seriesName}: ${value}%` // Combine label and value
    }
  },
  plotOptions: {
    pie: {
      donut: {
        size: '70%',
        labels: {
          show: true,
          total: {
            show: true,
            label: '2024',
            formatter: () => `${highestValue.value}%`
          }
        }
      }
    }
  }
})
</script>

<template>
  <div class="chart-container">
    <apexchart height="400" type="donut" :options="chartOptions" :series="series" />
  </div>
</template>
