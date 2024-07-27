<script setup>
import ReplacementReasonChart from '../charts/ReplacementReasonChart.vue'
</script>

<template>
  <div class="graph-container replacement" id="reasons">
    <div class="top padding">
      <h2>Replacement Reasons</h2>
      <div class="white-container year options">
        2024
        <svg class="icon arrow" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
          <title>triangle-down</title>
          <path d="M1 3H23L12 22" />
        </svg>
      </div>
    </div>

    <div class="chart-container">
      <ReplacementReasonChart />
    </div>
  </div>
</template>
