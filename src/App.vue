<script setup>
import { ref } from 'vue'
import MainContentHeader from './components/MainContentHeader.vue'

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
  <div class="container">
    <div class="header">
      <div class="logo">Logo</div>
    </div>

    <div class="sidebar">
      <div class="active">
        <div class="half-rounded-square"></div>
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
          <title>view-dashboard</title>
          <path d="M13,3V9H21V3M13,21H21V11H13M3,21H11V15H3M3,13H11V3H3V13Z" />
        </svg>
      </div>
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
        <title>file-document</title>
        <path
          d="M13,9H18.5L13,3.5V9M6,2H14L20,8V20A2,2 0 0,1 18,22H6C4.89,22 4,21.1 4,20V4C4,2.89 4.89,2 6,2M15,18V16H6V18H15M18,14V12H6V14H18Z"
        />
      </svg>
    </div>

    <div class="main-content">
      <MainContentHeader />

      <div class="first">
        <div class="graph-container replacement">
          <div class="top">
            <h2>Replacement</h2>
            <div class="white-container options">
              All Dealer
              <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                <title>triangle-down</title>
                <path d="M1 3H23L12 22" />
              </svg>
            </div>
          </div>

          <div>
            <apexchart type="bar" :options="chartOptions" :series="series"></apexchart>
          </div>
        </div>

        <div class="graph-container" id="production">
          <h2>Overall by Production year</h2>
          <div id="pie-chart"></div>
        </div>
      </div>

      <div class="graph-container" id="segment">
        <h2>Segment</h2>
        <div id="line-chart"></div>
      </div>

      <div class="graph-container replacement" id="reasons">
        <div class="top">
          <h2>Replacement Reasons</h2>
          <div class="white-container year options">
            2024
            <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
              <title>triangle-down</title>
              <path d="M1 3H23L12 22" />
            </svg>
          </div>
        </div>
        <div id="stacked-column-chart-2"></div>
      </div>

      <div class="graph-container replacement" id="region">
        <div class="top">
          <h3>Replacement ID by Region</h3>
          <div class="right">
            <div class="white-container date options">
              All Year
              <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                <title>triangle-down</title>
                <path d="M1 3H23L12 22" />
              </svg>
            </div>
            <div class="white-container options">
              Semua MD
              <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
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

        <table class="styled-table">
          <thead>
            <tr>
              <th>Header 1</th>
              <th>Header 2</th>
              <th>Header 3</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Data 1</td>
              <td>Data 2</td>
              <td>Data 3</td>
            </tr>
            <tr>
              <td>Data 4</td>
              <td>Data 5</td>
              <td>Data 6</td>
            </tr>
            <tr>
              <td>Data 7</td>
              <td>Data 8</td>
              <td>Data 9</td>
            </tr>
          </tbody>
        </table>
      </div>

      <div class="graph-container replacement" id="dealer">
        <div class="top">
          <h3>Replacement ID by Dealer</h3>
          <div class="right">
            <div class="white-container date options">
              All Year
              <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                <title>triangle-down</title>
                <path d="M1 3H23L12 22" />
              </svg>
            </div>
            <div class="white-container options">
              All Dealer
              <svg class="icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
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

        <table class="styled-table">
          <thead>
            <tr>
              <th>Header 1</th>
              <th>Header 2</th>
              <th>Header 3</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Data 1</td>
              <td>Data 2</td>
              <td>Data 3</td>
            </tr>
            <tr>
              <td>Data 4</td>
              <td>Data 5</td>
              <td>Data 6</td>
            </tr>
            <tr>
              <td>Data 7</td>
              <td>Data 8</td>
              <td>Data 9</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
