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
  <div class="slidev-layout focus h-full grid place-content-center" :style="style">
    <div class="my-auto flex flex-col justify-center items-center">
      <slot />
    </div>
  </div>
</template>