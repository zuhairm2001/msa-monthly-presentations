<script setup lang="ts">
import { useNav } from '@slidev/client'
import { computed } from 'vue'

const { currentPage, total, currentFrontmatter } = useNav()

const progress = computed(() => total.value > 1 ? (currentPage.value - 1) / (total.value - 1) : 1)
const hidden = computed(() => currentFrontmatter.value.layout === 'cover' || currentFrontmatter.value.chrome === false)
</script>

<template>
  <div class="progress" :class="{ hidden }" aria-hidden="true">
    <div class="bar" :style="{ transform: `scaleX(${progress})` }" />
  </div>
</template>

<style scoped>
.progress {
  position: absolute;
  inset: auto 0 0;
  height: 3px;
  transition: opacity 400ms var(--ease-out);
}

.progress.hidden {
  opacity: 0;
}

.bar {
  height: 100%;
  transform-origin: left;
  background: linear-gradient(90deg, var(--msa-violet), var(--ayu-accent));
  transition: transform 700ms var(--ease-out);
}
</style>
