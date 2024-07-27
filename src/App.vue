<script setup>
import MainContentHeader from './components/MainContentHeader.vue'
import ReplacementChart from './components/ReplacementChart.vue'
import ProductionChart from './components/ProductionChart.vue'
import ReplacementReasonChart from './components/ReplacementReasonChart.vue'
import SegmentChart from './components/SegmentChart.vue'
import TableTest from './components/TableTest.vue'
</script>

<template>
  <div class="container">
    <div class="header">
      <div class="logo">Logo</div>
    </div>

    <div class="sidebar">
      <div class="active">
        <div class="half-rounded-square"></div>
        <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
          <title>view-dashboard</title>
          <path d="M13,3V9H21V3M13,21H21V11H13M3,21H11V15H3M3,13H11V3H3V13Z" />
        </svg>
      </div>
      <div class="inactive">
        <div class="half-rounded-square"></div>
        <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
          <title>file-document</title>
          <path
            d="M13,9H18.5L13,3.5V9M6,2H14L20,8V20A2,2 0 0,1 18,22H6C4.89,22 4,21.1 4,20V4C4,2.89 4.89,2 6,2M15,18V16H6V18H15M18,14V12H6V14H18Z"
          />
        </svg>
      </div>
    </div>

    <div class="main-content">
      <MainContentHeader />

      <div class="first">
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

        <div class="graph-container" id="production">
          <h2 class="top border-bottom">Overall by Production year</h2>
          <div class="chart-container">
            <ProductionChart />
          </div>
        </div>
      </div>

      <div class="graph-container" id="segment">
        <h2 class="top padding">Segment</h2>
        <div class="chart-container">
          <SegmentChart />
        </div>
      </div>

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
    </div>
  </div>
</template>

<style scoped></style>
