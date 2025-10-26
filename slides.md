---
theme: default
background: "#0f0f0f"
class: text-center
highlighter: shiki
drawings:
  persist: false
transition: fade
layout: full
title: ViteConf 2025 - Key Takeaways
mdc: true
fonts:
  sans: "Inter"
  mono: "Fira Code"
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
#transition: slide-left
# duration of the presentation
duration: 6min
---

<div class="relative flex items-center justify-center" style="height: 300px;">
  <div class="absolute top--20 right-0 w-128 h-128 opacity-70" style="background: radial-gradient(circle at center, #00d4ff, #0ea5e9 30%, transparent 65%); filter: blur(80px);"></div>
  <div class="absolute bottom--20 left-0 w-128 h-128 opacity-70" style="background: radial-gradient(circle at center, #bd34fe, #7a23a1 30%, transparent 65%); filter: blur(80px);"></div>
  <div class="relative">
    <svg width="134" height="134" viewBox="0 0 134 134" fill="none" xmlns="http://www.w3.org/2000/svg" data-v-d1354460=""><g data-v-d1354460=""><rect class="vite-chip__background" x="1" y="1" width="132" height="132" rx="10" fill="black" fill-opacity="0.3" data-v-d1354460=""></rect><rect class="vite-chip__highlight" x="1" y="1" width="132" height="132" rx="10" fill="url(#linear-vite-chip-highlight)" fill-opacity="0.1" data-v-d1354460=""></rect><rect x="1" y="1" width="132" height="132" rx="10" stroke="#111111" stroke-opacity="0.2" stroke-width="1" data-v-d1354460=""></rect></g><g opacity="0.6" data-v-d1354460=""><rect x="1" y="1" width="132" height="132" rx="10" fill="#1E1E1E" fill-opacity="0.4" data-v-d1354460=""></rect><rect x="1" y="1" width="132" height="132" rx="10" stroke="url(#radial-edge)" stroke-width="1.15417" data-v-d1354460=""></rect><rect x="1" y="1" width="132" height="132" rx="10" stroke="url(#radial-edge-2)" stroke-opacity="0.1" stroke-width="1.15417" data-v-d1354460=""></rect></g><defs data-v-d1354460=""><linearGradient id="linear-vite-chip-highlight" x1="6.92498" y1="15.5812" x2="113.685" y2="116.571" gradientUnits="userSpaceOnUse" data-v-d1354460=""><stop offset="0" stop-opacity="0" data-v-d1354460=""></stop><stop offset="0.37" stop-color="white" data-v-d1354460=""></stop><stop offset="1" stop-opacity="0" data-v-d1354460=""></stop></linearGradient><radialGradient id="radial-edge" cx="0" cy="0" r="1" gradientUnits="userSpaceOnUse" gradientTransform="translate(95.2187 56.5541) rotate(110.653) scale(80.173)" data-v-d1354460=""><stop offset="0" stop-color="white" data-v-d1354460=""></stop><stop offset="1" stop-opacity="0" data-v-d1354460=""></stop></radialGradient><radialGradient id="radial-edge-2" cx="0" cy="0" r="1" gradientUnits="userSpaceOnUse" gradientTransform="translate(8.65624 122.919) rotate(-21.5713) scale(80.0504)" data-v-d1354460=""><stop offset="0" stop-color="white" data-v-d1354460=""></stop><stop offset="1" stop-opacity="0" data-v-d1354460=""></stop></radialGradient></defs></svg>
    <img class="absolute top-6 left-7 w-20" src="./public/assets/vite-logo.svg" />
  </div>
</div>
<h2 class="mt--8">ViteConf 2025</h2>

## Key Takeaways

<div class="opacity-70 text-sm mt-8">
Vite News Summary · October 2025
</div>

<!--
**SPEAKER NOTES - Slide 1 (30s)**

Hello everyone! Three weeks ago, I had the opportunity to attend ViteConf.

For those unfamiliar with Vite, I'll quickly explain what it is, then we'll look at the major announcements that will impact how we develop in the coming months.
-->

---
layout: full
---

<div 
  class="transition transition-500 mt-20 text-center scale-200"
  :class="$clicks > 0 && 'translate-x--90 scale-80 op80'"
>
    <h2>What is Vite?</h2>
</div>

<div class="grid grid-cols-2 gap-12 mt-12 items-center">
  <div class="text-left space-y-4">
    <div v-click="1" class="flex items-start gap-4">
      <img class="absolute right-0 top-0" src="./public/assets/fg.webp" />
      <div class="flex items-center gap-4 mt--4">
        <div class="text-4xl font-bold bg-gradient-to-r from-violet-400 to-yellow-400 bg-clip-text text-transparent">
          ⚡️
        </div>
        <p class="text-xl opacity-90 w-100">An ultra-fast <strong>build tool</strong></p>
      </div>
    </div>
  </div>

  <div class="text-left space-y-4">
    <div v-click="2" class="text-lg opacity-80 leading-relaxed">
      <p>Like Webpack or Parcel, but <strong>much faster</strong>.</p>
    </div>
    <div v-click="3" class="text-lg opacity-80 leading-relaxed">
      <p>It transforms and optimizes your JavaScript, TypeScript, Vue, React code, etc.</p>
    </div>
  </div>
</div>

<div v-click="4" class="text-left">

```bash
# Before Vite
npm run dev → 45s ⏳

# With Vite
npm run dev → 1.2s ⚡️
```

</div>

<!--
**SPEAKER NOTES - Slide 2 (30s)**

So Vite, to put it simply: it's a build tool.

You know, the tools that take your source code and transform it to work in the browser. Like Webpack that some of you may know.

The difference? Vite is MUCH faster.

Concretely: where a project took 45 seconds to start in development, with Vite it's 1 second.

This speed is what made it explode in adoption - today, it's become the standard for new web projects.

And the announcements from this ViteConf make Vite even faster.
-->

---
layout: full
---

<div class="flex items-center justify-center h-full">
  <div class="w-full max-w-6xl px-16">

  <h2 class="text-center mb-20">La transition vers Rolldown</h2>

<div class="relative">
  <div class="absolute top-12 left-0 right-0 h-0.5 bg-gradient-to-r from-violet-500 via-yellow-500 to-green-500 opacity-30"></div>

  <div class="grid grid-cols-3 gap-8">

<div v-click="1" class="relative flex flex-col items-center">
  <div class="w-24 h-24 rounded-full bg-violet-500 bg-opacity-20 border-2 border-violet-500 flex items-center justify-center mb-6 relative z-10">
    <img src="./public/assets/rollup-logo.svg" width="48" />
  </div>
  <h3 class="text-xl font-bold text-violet-400 mb-2">Rollup</h3>
  <p class="text-sm opacity-60 text-center">Aujourd'hui</p>
</div>

<div v-click="2" class="relative flex flex-col items-center">
  <div class="w-24 h-24 rounded-full bg-yellow-500 bg-opacity-20 border-2 border-yellow-500 flex items-center justify-center mb-6 relative z-10">
    <img src="./public/assets/lightning-down.svg" width="48" />
  </div>
  <h3 class="text-xl font-bold text-yellow-400 mb-2">Rolldown</h3>
  <p class="text-sm opacity-80 text-center font-semibold">Optionnel</p>
  <p class="text-sm opacity-60 text-center mt-1">Vite 6 · 2025</p>
</div>

<div v-click="3" class="relative flex flex-col items-center">
  <div class="w-28 h-28 rounded-full bg-green-500 bg-opacity-30 border-3 border-green-400 flex items-center justify-center mb-6 relative z-10 shadow-lg shadow-green-500/50">
    <img src="./public/assets/lightning-down.svg" width="56" />
  </div>
  <div class="absolute top--2 right-4 px-2 py-1 bg-green-500 rounded-full text-xs font-bold animate-pulse">
    NEW
  </div>
  <h3 class="text-2xl font-bold text-green-400 mb-2">Rolldown</h3>
  <p class="text-base opacity-90 text-center font-bold text-green-300">Par défaut</p>
  <p class="text-sm opacity-70 text-center mt-1 font-semibold">Vite 8 · Q1 2026</p>
</div>

  </div>
</div>

  </div>
</div>

<!--
**SPEAKER NOTES - Slide 3 (45s)**

Première annonce majeure : la transition vers Rolldown.

Rolldown est le nouveau bundler qui va remplacer Rollup dans Vite. C'est une réécriture complète en Rust pour des performances maximales.

La migration se fera progressivement :
- Aujourd'hui, Vite utilise Rollup, le bundler historique.
- À partir de Vite 6 début 2025, Rolldown sera disponible en option pour ceux qui veulent tester.
- Et à partir de Vite 8 au Q1 2026, Rolldown deviendra le choix par défaut.

Cette transition progressive permet à l'écosystème de s'adapter en douceur. Et comme vous allez le voir sur la prochaine slide, les gains de performance sont spectaculaires.
-->

---
layout: full
---

<div class="flex items-center justify-center h-full">
  <div class="w-full max-w-6xl px-16">
    <h2 v-hide class="text-center mb-16">Notre migration Rolldown</h2>
    <div :class="$clicks >=4 ? 'scale-50' : 'scale-100'" class="relative">
      <div class="flex justify-center items-center gap-16 mb-16">
        <div v-click="1" class="flex flex-col items-center">
          <div class="w-32 h-32 rounded-full bg-red-500 bg-opacity-20 border-2 border-red-500 flex items-center justify-center mb-6 relative z-10">
            <img src="./public/assets/rollup-logo.svg" width="64" />
          </div>
          <h3 class="text-xl font-bold text-red-400 mb-3">Rollup</h3>
          <div class="text-5xl font-bold opacity-80">
            1:24
          </div>
          <p class="text-sm opacity-50 mt-2">minutes</p>
        </div>
        <div v-click="2" class="text-6xl opacity-40">
          →
        </div>
        <div v-click="3" class="flex flex-col items-center">
          <div class="w-36 h-36 rounded-full bg-yellow-500 bg-opacity-25 border-3 border-yellow-400 flex items-center justify-center mb-6 relative z-10 shadow-lg shadow-yellow-500/40">
            <img src="./public/assets/lightning-down.svg" width="72" />
          </div>
          <h3 class="text-2xl font-bold text-yellow-400 mb-3">Rolldown</h3>
          <div class="text-6xl font-bold bg-gradient-to-r from-orange-400 to-yellow-400 bg-clip-text text-transparent">
            8s
          </div>
          <p class="text-sm opacity-60 mt-2 font-semibold">secondes</p>
        </div>
      </div>
      <div v-click="4" class="text-center mt-20">
        <template v-if="$clicks >= 4">
        <p>Moulining time reduced :</p>
          <AnimateNumber v-slot="{ number, target }" :value="97.4" :duration="500">
            <div
              class="text-8xl font-mono font-bold bg-gradient-to-r from-orange-400 to-yellow-400 bg-clip-text text-transparent"
              :style="{ transform: `scale(${1 + (number / target / 4)})` }"
            >
              {{ number.toFixed(1).padStart(4, '0') }}%
            </div>
          </AnimateNumber>
        </template>
      </div>
    </div>
  </div>
</div>

<!--
**SPEAKER NOTES - Slide 4 (45s)**

Nous avons testé Rolldown sur notre codebase, et les résultats sont spectaculaires.

Temps de build AVANT avec Rollup : 1 minute 39 secondes.

Temps de build APRÈS avec Rolldown : 7 secondes.

Ça représente une réduction de 97.4% du temps de build.

Concrètement, qu'est-ce que ça change ?

Pour les développeurs : vous itérez plus vite. Vous faites un changement, vous testez, c'est quasi instantané.

Pour les déploiements : on économise presque 2 minutes par build. Sur une journée avec 50 déploiements, ça fait 1h30 économisées rien que sur les builds.

Et ce n'est qu'avec Rolldown. Il y a encore mieux avec VitePlus.
-->

---
layout: full
---

<div class="flex items-center justify-center h-full">
  <div class="text-center">
    <div v-click="1" class="mb-8">
      <img src="./public/assets/vite+.svg" class="h-32 mx-auto" />
    </div>
    <p v-click="2" class="text-xl opacity-70 font-light mt-12">
      The Unified JavaScript Toolchain
    </p>
  </div>
</div>

<!--
**SPEAKER NOTES - Slide 5 (30s)**

Et maintenant, l'annonce la plus importante de ViteConf : VitePlus.

VitePlus, c'est la vision d'unifier tous nos outils de développement JavaScript en un seul toolchain ultra-rapide.

Aujourd'hui, nous utilisons de nombreux outils différents : Vite pour le build, ESLint pour le linting, Prettier pour le formatting, Vitest pour les tests... Chacun avec sa propre configuration.

VitePlus promet de tout regrouper en un seul outil. Voyons comment sur la slide suivante.
-->

---
layout: center
class: text-center
---

# OxLint vs ESLint

## Our Benchmarks

<div class="mt-12 grid grid-cols-2 gap-16 max-w-4xl mx-auto">

<div>
<p class="text-sm opacity-60 uppercase tracking-wider mb-4">ESLint</p>
<div class="text-7xl font-bold opacity-40">
8.3s
</div>
</div>

<div v-click="1">
<p class="text-sm opacity-60 uppercase tracking-wider mb-4">OxLint</p>
<div class="text-7xl font-bold bg-gradient-to-r from-green-400 to-yellow-400 bg-clip-text text-transparent">
0.2s
</div>
</div>

</div>

<div v-click="2" class="mt-16">
<div class="text-5xl font-bold text-green-400">
41x faster
</div>
<p class="text-lg opacity-70 mt-4">On our current codebase</p>
</div>

<!--
**SPEAKER NOTES - Slide 6 (45s)**

So, OxLint is the modern replacement for ESLint. We tested it on our code.

Results:
- ESLint took 8.3 seconds to analyze our code
- OxLint: 0.2 seconds

That's 41 times faster.

Why does it matter?

For developers: your editor shows errors in real-time, without lag.

For CI: we can lint more often without slowing down pipelines.

And OxLint detects more issues than ESLint - it implements TypeScript ESLint rules natively.

Same for OxFmt which replaces Prettier: same performance difference.
-->

---
layout: center
---

# Impact for Us

<div class="flex flex-wrap gap-12 mt-12 max-w-4xl mx-auto text-left">

<div v-click="1" class="p-6 w-96 h-48 bg-gray-800 bg-opacity-10 rounded-xl border-l-4 border-violet-400">
<h3 class="text-2xl font-bold mb-3 text-violet-300">📦 Build</h3>
<p class="text-lg opacity-90">Rolldown: <strong>-90%</strong> time · Faster deployments</p>
</div>

<div v-click="2" class="p-6 w-96 h-48 bg-gray-800 bg-opacity-10 rounded-xl border-l-4 border-yellow-400">
<h3 class="text-2xl font-bold mb-3 text-yellow-300">🔍 Lint</h3>
<p class="text-lg opacity-90">OxLint: <strong>41x faster</strong> · Instant feedback in dev</p>
</div>

<div v-click="3" class="p-6 w-96 h-48 bg-gray-800 bg-opacity-10 rounded-xl border-l-4 border-green-400">
<h3 class="text-2xl font-bold mb-3 text-green-300">🎯 Developer Experience</h3>
<p class="text-lg opacity-90">Less waiting = more productivity = happier teams</p>
</div>

<div v-click="4" class="p-6 w-96 h-48 bg-gray-800 bg-opacity-10 rounded-xl border-l-4 border-blue-400">
<h3 class="text-2xl font-bold mb-3 text-blue-300">🚀 Roadmap</h3>
<p class="text-lg opacity-90">Progressive migration to VitePlus in 2025</p>
</div>

</div>

<!--
**SPEAKER NOTES - Slide 7 (45s)**

So concretely, what are the key takeaways for us?

On BUILD: with Rolldown, we divide our build times by 10. This directly impacts our deployments and development velocity.

On LINT: OxLint is 41 times faster. This means less waiting, less friction, almost instantaneous feedback in the editor.

On overall DEVELOPER EXPERIENCE: all these gains accumulate. When you wait less, you iterate faster, you're less frustrated, you're more productive.

And on our ROADMAP: we'll progressively migrate to these tools in 2025. Rolldown is already tested and ready. VitePlus will arrive mid-year.

The JavaScript ecosystem is undergoing a major overhaul of its fundamental tools. And that's excellent news for all of us.
-->

---
layout: center
class: text-center
---

# Key Takeaways

<div class="mt-16 max-w-3xl mx-auto space-y-8">

<div v-click="1" class="text-3xl font-bold">
🚀 <span class="bg-gradient-to-r from-violet-400 to-yellow-400 bg-clip-text text-transparent">Rolldown</span>
</div>
<p v-click="1" class="text-xl opacity-80">Vite's new native build engine · <strong>-90%</strong> time</p>

<div v-click="2" class="text-3xl font-bold mt-8">
⚡️ <span class="bg-gradient-to-r from-yellow-400 to-green-400 bg-clip-text text-transparent">VitePlus</span>
</div>
<p v-click="2" class="text-xl opacity-80">The unified toolchain of the future · Based on <strong>Oxc</strong></p>

<div v-click="3" class="text-3xl font-bold mt-8">
✨ <span class="bg-gradient-to-r from-green-400 to-blue-400 bg-clip-text text-transparent">For Us</span>
</div>
<p v-click="3" class="text-xl opacity-80">Progressive migration · Immediate gains · Improved DX</p>

</div>

<!-- <div v-click="4" class="mt-16 text-sm opacity-50"> -->
<!-- Questions? -->
<!-- </div> -->

<!--
**SPEAKER NOTES - Slide 8 (30s)**

So, to summarize in 3 points:

1. ROLLDOWN: Vite's new core, written in Rust, which divides our build times by 10. It's available from early 2025.

2. VITEPLUS: the vision of a unified toolchain that replaces all our current tools. Based on Oxc, 10 to 100 times faster. Public alpha mid-2025.

3. FOR US: we'll migrate progressively, we already have measured gains on our codebase, and it will directly improve our daily development experience.

The JavaScript ecosystem is entering a new era of performance thanks to Rust. It's a major paradigm shift.

Thank you for your attention. Any questions?
-->
