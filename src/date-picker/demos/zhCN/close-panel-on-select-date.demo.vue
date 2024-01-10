<markdown>
# 选择年、月后，关闭年月面板
</markdown>

<template>
  <n-space vertical>
    <n-date-picker
      v-model:value="timestamp"
      close-panel-on-select-date
      type="date"
    />
    <n-date-picker
      v-model:value="timestamp"
      close-panel-on-select-date
      type="datetime"
    />
    <n-date-picker
      v-model:value="timestamp"
      close-panel-on-select-date
      type="week"
      clearable
    />
    <pre>{{ JSON.stringify(timestamp) }}</pre>
    <n-date-picker
      v-model:value="range"
      close-panel-on-select-date
      type="daterange"
    />
    <n-date-picker
      v-model:value="range"
      close-panel-on-select-date
      type="datetimerange"
    />
    <pre>{{ JSON.stringify(range) }}</pre>
  </n-space>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

export default defineComponent({
  setup () {
    return {
      timestamp: ref(1183135260000),
      range: ref<[number, number]>([1183135260000, Date.now()])
    }
  }
})
</script>
