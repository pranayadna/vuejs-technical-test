<script setup>
import ProductionChart from '../charts/ProductionChart.vue'
</script>

<template>
  <div class="graph-container" id="production">
    <h2 class="top border-bottom">Overall by Production year</h2>
    <div class="chart-container">
      <ProductionChart />
    </div>
  </div>
</template>
