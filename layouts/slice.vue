<script setup lang="ts">
import { computed } from 'vue'
import { handleBackground } from '@slidev/client/layoutHelper'
const props = defineProps({
  background: {
    default: '',
  },
})
const style = computed(() => handleBackground(props.background, true))
</script>

<template>
  <div class="slidev-layout slice" :style="style">
    <slot />
  </div>
</template>