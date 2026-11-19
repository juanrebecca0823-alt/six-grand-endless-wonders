<script setup lang="ts">
import { ref } from 'vue'

const tossKey = ref(0)
function tossAgain() {
  tossKey.value += 1
}
</script>

<template>
  <div class="rounded-xl border border-amber-200 bg-amber-50/75 p-3.5 flex flex-col gap-2.5">
    <div class="flex items-center justify-between">
      <div class="text-xs font-bold tracking-wider uppercase text-amber-800">
        Jiaobei · Moon-Block Divination
      </div>
      <button
        type="button"
        class="text-[10px] font-semibold px-2 py-0.5 rounded-full bg-amber-200/80 hover:bg-amber-300 text-amber-900 transition cursor-pointer"
        @click="tossAgain"
      >
        Toss Again
      </button>
    </div>

    <!-- Live tossing animation (same style as JourneyMap) -->
    <div class="rounded-lg bg-slate-900/90 border border-amber-400/40 px-3 py-1.5 flex items-center justify-between gap-2">
      <svg :key="tossKey" viewBox="0 0 120 72" width="96" height="58" class="shrink-0">
        <ellipse cx="38" cy="60" rx="18" ry="4" fill="rgba(0,0,0,0.4)" />
        <ellipse cx="82" cy="60" rx="18" ry="4" fill="rgba(0,0,0,0.4)" />
        <g class="block-left">
          <path d="M18,52 C22,36 46,34 54,50 C44,54 28,56 18,52 Z" fill="#fca5a5" stroke="#991b1b" stroke-width="2" />
          <path d="M22,51 C28,41 42,40 50,49" fill="none" stroke="#fef2f2" stroke-width="1.5" stroke-linecap="round" />
        </g>
        <g class="block-right">
          <path d="M66,50 C74,34 98,36 102,52 C92,56 76,54 66,50 Z" fill="#dc2626" stroke="#7f1d1d" stroke-width="2" />
          <path d="M72,45 C80,39 90,40 96,46" fill="none" stroke="#f87171" stroke-width="1.8" stroke-linecap="round" />
        </g>
        <circle cx="60" cy="20" r="2.2" fill="#fde047" class="sparkle s1" />
        <circle cx="44" cy="14" r="1.6" fill="#fde047" class="sparkle s2" />
        <circle cx="76" cy="16" r="1.8" fill="#fde047" class="sparkle s3" />
      </svg>
      <div class="text-right leading-snug">
        <div class="text-[11px] font-bold text-amber-300">Toss Demo · Shengjiao!</div>
        <div class="text-[10px] text-slate-300">Drop two crescent wooden blocks to seek guidance</div>
      </div>
    </div>

    <div class="flex items-center gap-2.5 bg-white/90 rounded-lg p-2 border border-amber-100 shadow-sm">
      <svg viewBox="0 0 96 42" width="68" height="30" class="shrink-0">
        <path d="M8,32 C12,14 34,12 42,28 C32,33 18,35 8,32 Z" fill="#fecaca" stroke="#991b1b" stroke-width="2" />
        <path d="M13,30 C20,21 32,20 38,27" fill="none" stroke="#fff" stroke-width="1.5" stroke-linecap="round" />
        <path d="M54,28 C62,12 84,14 88,32 C78,35 64,33 54,28 Z" fill="#dc2626" stroke="#7f1d1d" stroke-width="2" />
        <path d="M61,22 C69,17 78,18 83,24" fill="none" stroke="#f87171" stroke-width="1.8" stroke-linecap="round" />
      </svg>
      <div class="leading-tight">
        <div class="font-bold text-slate-800 text-xs">
          Shengjiao <span class="text-emerald-700">(Yes)</span>
        </div>
        <div class="text-[10.5px] text-slate-600 mt-0.5">
          1 Flat + 1 Curved · Approved / Good fortune
        </div>
      </div>
    </div>

    <div class="flex items-center gap-2.5 bg-white/90 rounded-lg p-2 border border-amber-100 shadow-sm">
      <svg viewBox="0 0 96 42" width="68" height="30" class="shrink-0">
        <path d="M8,32 C12,14 34,12 42,28 C32,33 18,35 8,32 Z" fill="#dc2626" stroke="#7f1d1d" stroke-width="2" />
        <path d="M14,24 C21,18 31,17 37,22" fill="none" stroke="#f87171" stroke-width="1.8" stroke-linecap="round" />
        <path d="M54,28 C62,12 84,14 88,32 C78,35 64,33 54,28 Z" fill="#dc2626" stroke="#7f1d1d" stroke-width="2" />
        <path d="M61,22 C69,17 78,18 83,24" fill="none" stroke="#f87171" stroke-width="1.8" stroke-linecap="round" />
      </svg>
      <div class="leading-tight">
        <div class="font-bold text-slate-800 text-xs">
          Yinjiao <span class="text-rose-700">(No)</span>
        </div>
        <div class="text-[10.5px] text-slate-600 mt-0.5">
          2 Curved Sides Up · Disagreement / Not now
        </div>
      </div>
    </div>

    <div class="flex items-center gap-2.5 bg-white/90 rounded-lg p-2 border border-amber-100 shadow-sm">
      <svg viewBox="0 0 96 42" width="68" height="30" class="shrink-0">
        <path d="M8,32 C12,14 34,12 42,28 C32,33 18,35 8,32 Z" fill="#fecaca" stroke="#991b1b" stroke-width="2" />
        <path d="M13,30 C20,21 32,20 38,27" fill="none" stroke="#fff" stroke-width="1.5" stroke-linecap="round" />
        <path d="M54,28 C62,12 84,14 88,32 C78,35 64,33 54,28 Z" fill="#fecaca" stroke="#991b1b" stroke-width="2" />
        <path d="M59,27 C66,20 78,21 84,30" fill="none" stroke="#fff" stroke-width="1.5" stroke-linecap="round" />
      </svg>
      <div class="leading-tight">
        <div class="font-bold text-slate-800 text-xs">
          Xiaojiao <span class="text-amber-700">(Laughing)</span>
        </div>
        <div class="text-[10.5px] text-slate-600 mt-0.5">
          2 Flat Sides Up · Unclear, clarify & toss again
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.block-left { transform-origin: 36px 48px; animation: toss-left 1.3s cubic-bezier(.22,1,.36,1) forwards; }
.block-right { transform-origin: 84px 48px; animation: toss-right 1.3s cubic-bezier(.22,1,.36,1) forwards; }
@keyframes toss-left {
  0% { transform: translateY(-26px) rotate(-140deg) scale(.85); opacity: 0; }
  45% { transform: translateY(-32px) rotate(40deg) scale(1.05); opacity: 1; }
  75% { transform: translateY(2px) rotate(-8deg); }
  100% { transform: translateY(0) rotate(0deg); }
}
@keyframes toss-right {
  0% { transform: translateY(-30px) rotate(160deg) scale(.85); opacity: 0; }
  50% { transform: translateY(-34px) rotate(-35deg) scale(1.05); opacity: 1; }
  78% { transform: translateY(2px) rotate(8deg); }
  100% { transform: translateY(0) rotate(0deg); }
}
.sparkle { opacity: 0; animation: pop-sparkle .8s ease-out 1.1s forwards; }
.s2 { animation-delay: 1.2s; }
.s3 { animation-delay: 1.3s; }
@keyframes pop-sparkle {
  0% { opacity: 0; transform: scale(0); }
  60% { opacity: 1; transform: scale(1.3); }
  100% { opacity: .9; transform: scale(1); }
}
</style>
