<script setup lang="ts">
import { computed } from 'vue'
import { handleBackground } from '@slidev/client/layoutHelper'
const props = defineProps<{
  imageSrc?: string
  headerMessage?: string
  speakerName?: string
  jobTitle?: string
  info1?: string
  info2?: string
  social1?: string
  social2?: string
  social3?: string
}>()
const style = computed(() => handleBackground(props.imageSrc, false))
</script>

<template>
  <div class="slidev-layout speaker-info p-0">
    <div class="flex h-full">
      <div class="w-1/2 h-full flex flex-col justify-end" :style="style">
      </div>
      <div class="w-1/2 flex flex-col justify-between items-end px-8 py-16">
        <h1 v-if="headerMessage" class="flex">{{ headerMessage }}</h1>

        <div class="flex flex-col justify-end items-end text-right py-16">
          <h2 class="font-extrabold">{{ speakerName }}</h2>

          <div class="text-2xl space-y-2 mt-4">
            <p class="jobTitle">{{ jobTitle }}</p>
            <p class="info-1">{{ info1 }}</p>
            <p class="info-2">{{ info2 }}</p>
          </div>

          <div class="text-2xl space-y-2 mt-4">
            <p class="social social-1">{{ social1 }}</p>
            <p class="social social-2">{{ social2 }}</p>
            <p class="social social-3">{{ social3 }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>