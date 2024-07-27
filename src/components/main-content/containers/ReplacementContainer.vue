<script setup>
import ReplacementChart from '../charts/ReplacementChart.vue'
</script>

<template>
  <div class="graph-container replacement">
    <div class="top border-bottom">
      <h2>Replacement</h2>
      <div class="white-container options">
        All Dealer
        <svg class="icon arrow" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
          <title>triangle-down</title>
          <path d="M1 3H23L12 22" />
        </svg>
      </div>
    </div>

    <div class="chart-container">
      <ReplacementChart />
    </div>
  </div>
</template>
