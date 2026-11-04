<script setup lang="ts">
withDefaults(defineProps<{
  src: string
  url: string
  alt?: string
  maxHeight?: string
}>(), {
  alt: '',
  maxHeight: '440px',
})
</script>

<template>
  <figure class="browser">
    <div class="bar">
      <span class="dots"><i /><i /><i /></span>
      <span class="addr mono"><span class="i-fluent-lock-closed-12-filled" />{{ url }}</span>
    </div>
    <div class="view" :style="{ maxHeight }">
      <img :src="src" :alt="alt">
    </div>
  </figure>
</template>

<style scoped>
.browser {
  width: 100%;
  margin: 0;
  overflow: hidden;
  border: 1px solid var(--ayu-line);
  border-radius: 14px;
  background: var(--ayu-panel);
  box-shadow:
    0 30px 60px -20px rgb(0 0 0 / 0.65),
    0 0 0 1px rgb(255 255 255 / 0.02);
  animation: tilt-in 1000ms var(--ease-out) both 160ms;
}

@keyframes tilt-in {
  from {
    opacity: 0;
    transform: perspective(1400px) rotateY(-12deg) translateX(40px) scale(0.96);
  }
}

.bar {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 0.6rem 0.9rem;
  border-bottom: 1px solid var(--ayu-line);
}

.dots {
  display: flex;
  gap: 6px;
}

.dots i {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background: var(--ayu-line);
}

.addr {
  flex: 1;
  display: inline-flex;
  align-items: center;
  gap: 0.45rem;
  padding: 0.25rem 0.75rem;
  border-radius: 999px;
  font-size: 0.75rem;
  color: var(--ayu-muted);
  background: var(--ayu-bg);
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

.addr span {
  color: var(--ayu-green);
}

.view {
  overflow: hidden;
}

.view img {
  display: block;
  width: 100%;
  object-fit: cover;
  object-position: top;
}
</style>
