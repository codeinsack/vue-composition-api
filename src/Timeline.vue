<template>
  <div class="is-primary panel">
    <div class="panel-tabs">
      <a v-for="period in periods" :key="period">
        {{ period }}
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { Period } from './types'

export default defineComponent({
  setup() {
    const periods: Period[] = ['today', 'this week', 'this month']

    return {
      periods,
    }
  }
})
</script>