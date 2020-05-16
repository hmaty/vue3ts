<template>
  <button @click="increment1">
    counts[0] is: {{ state.counts[0] }}
  </button>
  <button @click="increment2">
    counts[1] is: {{ state.counts[1] }}
  </button>
</template>

<script>
import { reactive } from 'vue'

export default {
  setup() {
    const state = reactive({
      counts: [100, 200],
    })

    function increment1() {
      state.counts[0]++
    }

    function increment2() {
      state.counts[1]++
    }

    return {
      state,
      increment1,
      increment2,
    }
  }
}
</script>
