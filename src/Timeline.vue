<template>
  <div class="is-primary panel">
    <div class="panel-tabs">
      <a
        data-test="period"
        v-for="period in periods"
        :key="period"
      >
        {{ period }}
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { Periods } from './types'

export default defineComponent({
  setup() {
    const periods: Periods[] = ['today', 'this week', 'this month']

    return {
      periods,
    }
  }
})
</script>