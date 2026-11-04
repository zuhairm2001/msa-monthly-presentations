<template>
  <div class="slidev-layout cover">
    <div class="backdrop" aria-hidden="true">
      <div class="orb orb-purple drift" />
      <div class="orb orb-gold drift" />
      <div class="grid" />
    </div>

    <header class="brandbar rise">
      <MsLogo :size="22" wordmark animate />
      <span class="divider" />
      <MsaLogo :size="34" glow />
    </header>

    <div class="cover-body">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.cover {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  overflow: hidden;
  isolation: isolate;
}

.backdrop {
  position: absolute;
  inset: 0;
  z-index: -1;
}

.orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(80px);
}

.orb-purple {
  width: 720px;
  height: 720px;
  top: -260px;
  right: -180px;
  background: radial-gradient(circle, color-mix(in srgb, var(--msa-violet) 75%, transparent), transparent 68%);
}

.orb-gold {
  width: 520px;
  height: 520px;
  bottom: -320px;
  left: -140px;
  background: radial-gradient(circle, color-mix(in srgb, var(--ayu-accent) 26%, transparent), transparent 70%);
  animation-delay: -9s !important;
}

.drift {
  animation: drift 22s var(--ease-in-out) infinite alternate;
}

@keyframes drift {
  to {
    transform: translate(-40px, 30px) scale(1.06);
  }
}

.grid {
  position: absolute;
  inset: 0;
  background-image: radial-gradient(color-mix(in srgb, var(--ayu-fg) 16%, transparent) 1px, transparent 1px);
  background-size: 28px 28px;
  mask-image: radial-gradient(ellipse 70% 80% at 75% 20%, black, transparent 75%);
}

.brandbar {
  display: flex;
  align-items: center;
  gap: 1.4rem;
}

.divider {
  width: 1px;
  height: 30px;
  background: color-mix(in srgb, var(--ayu-fg) 30%, transparent);
}

.cover-body {
  display: flex;
  flex-direction: column;
  gap: 1.1rem;
}

.cover-body :deep(h1) {
  font-size: 4.4rem;
  font-weight: 700;
  line-height: 1.02;
  letter-spacing: -0.03em;
  max-width: 15ch;
}
</style>
