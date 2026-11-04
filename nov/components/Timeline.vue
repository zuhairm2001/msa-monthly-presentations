<script setup lang="ts">
import type { ClicksInfo } from '@slidev/types'
import { useSlideContext } from '@slidev/client'
import { computed, onMounted, onUnmounted, shallowRef } from 'vue'

interface Step {
  title: string
  body?: string
  meta?: string
  note?: string
  span?: number
}

const props = withDefaults(defineProps<{
  steps: Step[]
  tone?: string
}>(), {
  tone: 'accent',
})

// The first step is visible on enter; each further step takes one click.
// Registered in `onMounted`, the same phase `v-click` uses, so ordering with
// sibling clicks holds and a remount (e.g. under view transitions) re-registers cleanly.
const { $clicksContext } = useSlideContext()
const id = Symbol('timeline')
const info = shallowRef<ClicksInfo | null>(null)
onMounted(() => {
  info.value = $clicksContext.calculateSince('+1', props.steps.length - 1)
  $clicksContext.register(id, info.value)
})
onUnmounted(() => $clicksContext.unregister(id))

const last = props.steps.length - 1
const shown = computed(() => info.value
  ? 1 + Math.min(last, Math.max(0, $clicksContext.current - info.value.start + 1))
  : 1)
const total = props.steps.reduce((sum, s) => sum + (s.span ?? 1), 0)
const progress = computed(() => props.steps.slice(0, shown.value).reduce((sum, s) => sum + (s.span ?? 1), 0) / total)
</script>

<template>
  <div class="timeline" :class="`tone-${tone}`">
    <div class="rail">
      <div class="fill" :style="{ transform: `scaleX(${progress})` }" />
    </div>
    <ol>
      <li
        v-for="(step, i) in steps"
        :key="step.title"
        class="slidev-vclick-target"
        :class="{ 'slidev-vclick-hidden': i >= shown, 'current': i === shown - 1 }"
        :style="{ flexGrow: step.span ?? 1 }"
      >
        <span class="node mono">{{ i + 1 }}</span>
        <span v-if="step.meta" class="meta mono">{{ step.meta }}</span>
        <h3>{{ step.title }}</h3>
        <p v-if="step.body">{{ step.body }}</p>
        <p v-if="step.note" class="note">{{ step.note }}</p>
      </li>
    </ol>
  </div>
</template>

<style scoped>
.timeline {
  position: relative;
  --node: 2.1rem;
}

.rail {
  position: absolute;
  top: calc(var(--node) / 2 - 1px);
  left: 0;
  right: 0;
  height: 3px;
  border-radius: 3px;
  background: var(--ayu-line);
  overflow: hidden;
}

.fill {
  height: 100%;
  transform-origin: left;
  background: linear-gradient(90deg, var(--msa-violet), var(--tone));
  transition: transform 900ms var(--ease-out);
}

ol {
  display: flex;
  gap: 1.25rem;
  margin: 0;
  padding: 0;
  list-style: none;
}

li {
  flex-basis: 0;
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
  min-width: 0;
}

.node {
  position: relative;
  display: grid;
  place-items: center;
  width: var(--node);
  height: var(--node);
  margin-bottom: 0.65rem;
  border-radius: 50%;
  font-size: 0.9rem;
  font-weight: 700;
  color: var(--ayu-bg);
  background: var(--tone);
  box-shadow: 0 0 0 5px var(--ayu-bg);
  transition: box-shadow 600ms var(--ease-out);
}

li.current .node {
  box-shadow:
    0 0 0 5px var(--ayu-bg),
    0 0 0 9px color-mix(in srgb, var(--tone) 35%, transparent);
}

.meta {
  font-size: 0.78rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--tone);
}

h3 {
  font-size: 1.3rem;
}

p {
  font-size: 1.06rem;
  line-height: 1.45;
  color: var(--ayu-muted);
}

p.note {
  color: var(--ayu-fg);
}
</style>
