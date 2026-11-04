<script setup lang="ts">
import { useSlideContext } from '@slidev/client'

const { $frontmatter } = useSlideContext()
</script>

<template>
  <div class="slidev-layout split">
    <div class="split-main">
      <p v-if="$frontmatter.kicker" class="kicker rise">{{ $frontmatter.kicker }}</p>
      <slot />
    </div>
    <div class="split-aside">
      <slot name="right" />
    </div>
  </div>
</template>

<style scoped>
.split {
  display: grid;
  grid-template-columns: minmax(0, 0.9fr) minmax(0, 1.1fr);
  gap: 3.5rem;
  align-items: center;
}

.split-main {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.split-aside {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 0;
}
</style>
