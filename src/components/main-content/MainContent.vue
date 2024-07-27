<script setup>
import ReplacementContainer from './containers/ReplacementContainer.vue'
import ProductionContainer from './containers/ProductionContainer.vue'
import SegmentContainer from './containers/SegmentContainer.vue'
import ReplacementReasonContainer from './containers/ReplacementReasonContainer.vue'
import TableContainer from './containers/TableContainer.vue'
import MainHeader from './MainHeader.vue'
</script>

<template>
  <div class="main-content">
    <MainHeader />

    <div class="first">
      <ReplacementContainer />
      <ProductionContainer />
    </div>

    <SegmentContainer />
    <ReplacementReasonContainer />
    <TableContainer />
  </div>
</template>
