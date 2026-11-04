<script setup lang="ts">
import { useSlideContext } from '@slidev/client'

const { $frontmatter } = useSlideContext()
</script>

<template>
  <div class="slidev-layout default">
    <p v-if="$frontmatter.kicker" class="kicker rise">{{ $frontmatter.kicker }}</p>
    <slot />
  </div>
</template>
