<script setup>
import { ref, computed } from 'vue'

const series = ref([38, 15, 22, 25])
const labels = ['2024', '2023', '2022', 'Others']
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
    offsetY: 15,
    fontSize: '23px',
    itemMargin: {
      horizontal: 50,
      vertical: 15
    },
    formatter: (seriesName, opts) => {
      const index = opts.seriesIndex
      const value = series.value[index]
      return `${seriesName}: ${value}%`
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
    <apexchart height="450" type="donut" :options="chartOptions" :series="series" />
</template>
