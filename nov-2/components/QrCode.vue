<script setup lang="ts">
import QRCode from 'qrcode'
import { ref, watchEffect } from 'vue'

const props = withDefaults(defineProps<{
  url: string
  label?: string
  caption?: string
  size?: number
  tone?: string
}>(), {
  size: 200,
  tone: 'accent',
})

const svg = ref('')

watchEffect(async () => {
  svg.value = await QRCode.toString(props.url, {
    type: 'svg',
    margin: 0,
    errorCorrectionLevel: 'M',
    color: { dark: '#0d1017', light: '#ffffff' },
  })
})
</script>

<template>
  <figure class="qr" :class="`tone-${tone}`">
    <div class="frame" :style="{ width: `${size}px` }">
      <div class="tile" v-html="svg" />
      <i v-for="c in ['tl', 'tr', 'bl', 'br']" :key="c" class="corner" :class="c" />
    </div>
    <figcaption v-if="label || caption">
      <strong v-if="label">{{ label }}</strong>
      <span v-if="caption" class="mono">{{ caption }}</span>
    </figcaption>
  </figure>
</template>

<style scoped>
.qr {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.9rem;
  margin: 0;
}

.frame {
  position: relative;
  padding: 14px;
}

.tile {
  padding: 12px;
  background: #fff;
  border-radius: 12px;
  line-height: 0;
}

.tile :deep(svg) {
  width: 100%;
  height: auto;
}

.corner {
  position: absolute;
  width: 22px;
  height: 22px;
  border: 3px solid var(--tone);
  animation: lock 900ms var(--ease-out) both 250ms;
}

.tl { top: 0; left: 0; border-right: 0; border-bottom: 0; border-top-left-radius: 10px; --dx: -10px; --dy: -10px; }
.tr { top: 0; right: 0; border-left: 0; border-bottom: 0; border-top-right-radius: 10px; --dx: 10px; --dy: -10px; }
.bl { bottom: 0; left: 0; border-right: 0; border-top: 0; border-bottom-left-radius: 10px; --dx: -10px; --dy: 10px; }
.br { bottom: 0; right: 0; border-left: 0; border-top: 0; border-bottom-right-radius: 10px; --dx: 10px; --dy: 10px; }

@keyframes lock {
  from {
    opacity: 0;
    transform: translate(var(--dx), var(--dy));
  }
}

figcaption {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.2rem;
  text-align: center;
}

figcaption strong {
  font-size: 1.1rem;
}

figcaption .mono {
  font-size: 0.82rem;
  color: var(--ayu-muted);
}
</style>
