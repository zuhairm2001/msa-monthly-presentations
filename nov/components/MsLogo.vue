<script setup lang="ts">
withDefaults(defineProps<{
  size?: number
  wordmark?: boolean
  animate?: boolean
}>(), {
  size: 22,
  wordmark: false,
  animate: false,
})

const squares = [
  { x: 0, y: 0, fill: '#f25022' },
  { x: 11, y: 0, fill: '#7fba00' },
  { x: 0, y: 11, fill: '#00a4ef' },
  { x: 11, y: 11, fill: '#ffb900' },
]
</script>

<template>
  <span class="ms-logo" :class="{ animate }" :style="{ '--s': `${size}px` }">
    <svg :width="size" :height="size" viewBox="0 0 21 21" aria-label="Microsoft" role="img">
      <rect
        v-for="(sq, i) in squares"
        :key="i"
        :x="sq.x"
        :y="sq.y"
        width="10"
        height="10"
        :fill="sq.fill"
        :style="{ '--i': i }"
      />
    </svg>
    <span v-if="wordmark" class="ms-word">Microsoft</span>
  </span>
</template>

<style scoped>
.ms-logo {
  display: inline-flex;
  align-items: center;
  gap: calc(var(--s) * 0.45);
}

.ms-word {
  font-family: 'Segoe UI', 'Open Sans', sans-serif;
  font-weight: 600;
  font-size: calc(var(--s) * 0.95);
  letter-spacing: -0.01em;
  color: var(--ayu-fg-strong);
}

.animate rect {
  transform-box: fill-box;
  transform-origin: center;
  animation: pop 640ms var(--ease-out) both;
  animation-delay: calc(var(--i) * 80ms + 150ms);
}

@keyframes pop {
  from {
    opacity: 0;
    transform: scale(0.4);
  }
}
</style>
