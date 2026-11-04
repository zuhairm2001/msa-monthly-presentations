<script setup lang="ts">
import { useSlideContext } from '@slidev/client'

const { $frontmatter } = useSlideContext()
</script>

<template>
  <div class="slidev-layout center">
    <p v-if="$frontmatter.kicker" class="kicker rise">{{ $frontmatter.kicker }}</p>
    <slot />
  </div>
</template>

<style scoped>
.center {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.center :deep(h1 + p) {
  margin-left: auto;
  margin-right: auto;
}
</style>
