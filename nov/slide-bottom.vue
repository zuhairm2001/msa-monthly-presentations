<script setup lang="ts">
import { slideHeight, slideWidth, useSlideContext } from '@slidev/client'
import { computed } from 'vue'

const { $frontmatter, $page, $nav } = useSlideContext()

const visible = computed(() => $frontmatter.layout !== 'cover' && $frontmatter.chrome !== false)
</script>

<template>
  <footer v-if="visible" class="chrome" :style="{ width: `${slideWidth}px`, top: `${slideHeight - 52}px` }">
    <MsaLogo :size="22" class="footer-mark" />
    <span class="mono meta">
      MSA Monthly Connect · Nov 2026
      <span class="page">{{ String($page).padStart(2, '0') }}<span class="of">/{{ $nav.total }}</span></span>
    </span>
  </footer>
</template>

<style scoped>
/* The slide-bottom layer has no size of its own, so the footer is laid out against the canvas. */
.chrome {
  position: absolute;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
  box-sizing: border-box;
  padding: 0 4.5rem;
  pointer-events: none;
}

.footer-mark {
  opacity: 0.75;
}

.meta {
  display: inline-flex;
  align-items: baseline;
  gap: 1rem;
  font-size: 0.72rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--ayu-gray);
}

.page {
  color: var(--ayu-accent);
  font-weight: 600;
}

.of {
  color: var(--ayu-gray);
  font-weight: 400;
}
</style>
