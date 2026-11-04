<script setup lang="ts">
withDefaults(defineProps<{
  title: string
  tone?: string
  icon?: string
  n?: string | number
}>(), {
  tone: 'accent',
})
</script>

<template>
  <article class="card" :class="`tone-${tone}`">
    <div v-if="icon || n !== undefined" class="badge">
      <span v-if="icon" :class="icon" />
      <span v-else class="mono">{{ n }}</span>
    </div>
    <h3>{{ title }}</h3>
    <div class="body">
      <slot />
    </div>
    <footer v-if="$slots.foot" class="foot mono">
      <slot name="foot" />
    </footer>
  </article>
</template>

<style scoped>
.card {
  position: relative;
  display: flex;
  flex-direction: column;
  gap: 0.55rem;
  padding: 1.25rem 1.3rem 1.2rem;
  background: var(--ayu-lift);
  border: 1px solid var(--ayu-line);
  border-radius: 14px;
  overflow: hidden;
}

.card::before {
  content: '';
  position: absolute;
  inset: 0 0 auto;
  height: 3px;
  background: linear-gradient(90deg, var(--tone), transparent 85%);
}

.badge {
  display: grid;
  place-items: center;
  width: 2.4rem;
  height: 2.4rem;
  border-radius: 10px;
  font-size: 1.35rem;
  font-weight: 700;
  color: var(--tone);
  background: color-mix(in srgb, var(--tone) 14%, transparent);
}

.badge .mono {
  font-size: 1.05rem;
}

.body {
  font-size: 1.12rem;
  line-height: 1.45;
  color: var(--ayu-muted);
}

.foot {
  margin-top: auto;
  padding-top: 0.65rem;
  border-top: 1px dashed var(--ayu-line);
  font-size: 0.85rem;
  color: var(--tone);
}
</style>
