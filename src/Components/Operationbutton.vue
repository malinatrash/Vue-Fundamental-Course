<script setup>
import { ref, computed } from 'vue'
const props = defineProps({
  operation: {
    type: String,
    default: '+',
  },
  activeOperation: {
    type: String
  }
})
const emit = defineEmits(['clicked'])
const cls = computed(() => {
  return {
    'btn-primary' : props.operation === props.activeOperation,
    'btn-outline-primary' : props.operation !== props.activeOperation
  }
})
</script>

<template>
  <button
      :class="cls"
      class="btn w-100"
      @click="emit('clicked')"
      value="c.value"
  >
    {{ operation }}
  </button>
</template>

<style></style>




