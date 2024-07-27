<script setup>
import TableTest from '../TableTest.vue'
</script>

<template>
  <div class="graph-container replacement" id="region">
    <div class="top padding">
      <h3>Replacement ID by Region</h3>
      <div class="right">
        <div class="white-container date options">
          All Year
          <svg class="icon arrow" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <title>triangle-down</title>
            <path d="M1 3H23L12 22" />
          </svg>
        </div>
        <div class="white-container options">
          Semua MD
          <svg class="icon arrow" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <title>triangle-down</title>
            <path d="M1 3H23L12 22" />
          </svg>
        </div>
        <div class="white-container download-csv">
          Download CSV
          <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <title>file-download</title>
            <path
              d="M14,2H6C4.89,2 4,2.89 4,4V20C4,21.11 4.89,22 6,22H18C19.11,22 20,21.11 20,20V8L14,2M12,19L8,15H10.5V12H13.5V15H16L12,19M13,9V3.5L18.5,9H13Z"
            />
          </svg>
        </div>
      </div>
    </div>

    <TableTest />
  </div>

  <div class="graph-container replacement" id="dealer">
    <div class="top padding">
      <h3>Replacement ID by Dealer</h3>
      <div class="right">
        <div class="white-container date options">
          All Year
          <svg class="icon arrow" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <title>triangle-down</title>
            <path d="M1 3H23L12 22" />
          </svg>
        </div>
        <div class="white-container options">
          All Dealer
          <svg class="icon arrow" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <title>triangle-down</title>
            <path d="M1 3H23L12 22" />
          </svg>
        </div>
        <div class="white-container download-csv">
          Download CSV
          <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
            <title>file-download</title>
            <path
              d="M14,2H6C4.89,2 4,2.89 4,4V20C4,21.11 4.89,22 6,22H18C19.11,22 20,21.11 20,20V8L14,2M12,19L8,15H10.5V12H13.5V15H16L12,19M13,9V3.5L18.5,9H13Z"
            />
          </svg>
        </div>
      </div>
    </div>

    <TableTest />
  </div>
</template>
