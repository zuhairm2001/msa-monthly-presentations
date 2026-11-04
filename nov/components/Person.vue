<script setup lang="ts">
withDefaults(defineProps<{
  name: string
  img: string
  role?: string
  team?: string
  tone?: string
  size?: number
  vt?: string
}>(), {
  tone: 'accent',
  size: 168,
})
</script>

<template>
  <figure class="person" :class="`tone-${tone}`">
    <div class="ring" :style="{ width: `${size}px`, height: `${size}px`, viewTransitionName: vt }">
      <img :src="img" :alt="name">
    </div>
    <figcaption>
      <strong class="name">{{ name }}</strong>
      <span v-if="role" class="role">{{ role }}</span>
      <span v-if="team" class="team">{{ team }}</span>
      <span class="org"><MsLogo :size="13" /> Microsoft</span>
    </figcaption>
  </figure>
</template>

<style scoped>
.person {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.1rem;
  margin: 0;
  text-align: center;
}

.ring {
  border-radius: 50%;
  padding: 5px;
  background: conic-gradient(from 210deg, var(--tone), var(--msa-violet), var(--tone));
}

.ring img {
  display: block;
  width: 100%;
  height: 100%;
  border-radius: 50%;
  object-fit: cover;
  border: 4px solid var(--ayu-bg);
  background: var(--ayu-panel);
}

figcaption {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.15rem;
}

.name {
  font-size: 1.45rem;
  font-weight: 600;
  color: var(--ayu-fg-strong);
}

.role {
  font-size: 1.05rem;
  color: var(--tone);
}

.team {
  font-size: 0.98rem;
  color: var(--ayu-fg);
}

.org {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  margin-top: 0.35rem;
  font-size: 0.9rem;
  color: var(--ayu-muted);
}
</style>
