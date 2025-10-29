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
**SPEAKER NOTES - Slide 1 (25s)**

Hi everyone! Three weeks ago, I had the chance to attend ViteConf.

For those who don't know Vite, I'll quickly explain what it is. Then we'll look at the major announcements that will change how we develop in the coming months.
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

<div class="mt-8 h-full">
  <img class="absolute right-0 top-0" src="./public/assets/fg.webp" />
  <div v-click="1" class="max-w-2xl">
    <div class="border-l-5 border-violet-400 pl-6">
      <p class="text-3xl font-light opacity-90" style="line-height: 40px;">
        A build tool that serves code via native <strong>ESM</strong> during development and bundles with <strong>Rollup</strong> for production.
      </p>
    </div>
  </div>
</div>

<!--
**SPEAKER NOTES - Slide 2 (25s)**

  So, what's Vite?

  Simply put: it's a build tool.

  During development, it serves your code directly using native ES modules. No bundling upfront. That's why the dev server starts instantly.

  For production, it bundles everything with Rollup for optimized delivery.

  Fast dev, optimized builds. That's Vite.

  -->

---
layout: full
---

<div class="flex items-center justify-center h-full">
  <div class="w-full max-w-6xl px-16">

  <h2 class="text-center mb-20">The Transition to Rolldown</h2>

<div class="relative">
  <div class="absolute top-12 left-0 right-0 h-0.5 bg-gradient-to-r from-violet-500 via-yellow-500 to-green-500 opacity-30"></div>

  <div class="grid grid-cols-3 gap-8">

<div class="relative flex flex-col items-center">
  <div class="w-24 h-24 rounded-full border-2 border-violet-500 mb-6 relative z-10">
    <div class="w-full h-full rounded-full flex items-center justify-center" style="background: linear-gradient(rgba(139, 92, 246, 0.2), rgba(139, 92, 246, 0.2)), #0f0f0f;">
      <img src="./public/assets/rollup-logo.svg" width="48" />
    </div>
  </div>
  <h3 class="text-xl font-bold text-violet-400">Rollup</h3>
  <p class="text-sm opacity-80 text-center font-semibold !mt-1">By Default</p>
  <p class="text-sm opacity-60 text-center">Today</p>
</div>

<div class="relative flex flex-col items-center">
  <div class="mt--2 w-28 h-28 rounded-full border-2 border-yellow-500 mb-6 relative z-10">
    <div class="w-full h-full rounded-full flex items-center justify-center" style="background: linear-gradient(rgba(234, 179, 8, 0.2), rgba(234, 179, 8, 0.2)), #0f0f0f;">
      <img src="./public/assets/lightning-down.svg" width="48" />
    </div>
  </div>
  <h3 class="text-xl font-bold text-yellow-400 text-center">Rolldown</h3>
  <p class="text-sm opacity-80 text-center font-semibold !mt-1">Optional</p>
  <p class="text-sm opacity-60 text-center !mt-3">Vite 7 · June 2025</p>
</div>

<div v-click="1" class="relative flex flex-col items-center">
  <div class="mt--5 w-32 h-32 rounded-full border-3 border-green-400 mb-6 relative z-10 shadow-lg shadow-green-500/50">
    <div class="w-full h-full rounded-full flex items-center justify-center" style="background: linear-gradient(rgba(34, 197, 94, 0.25), rgba(34, 197, 94, 0.25)), #0f0f0f;">
      <img src="./public/assets/lightning-down.svg" width="56" />
    </div>
  </div>
  <div class="absolute top--8 right-6 px-2 py-1 bg-green-500 rounded-full text-xs font-bold animate-pulse">
    NEW
  </div>
  <h3 class="text-2xl font-bold text-green-400">Rolldown</h3>
  <p class="text-sm opacity-90 text-center font-bold text-green-300 !mt-1">By Default</p>
  <p class="text-sm opacity-70 text-center font-semibold !mt-2">Vite 8 · Q1 2026</p>
</div>

  </div>
</div>

  </div>
</div>

<!--
**SPEAKER NOTES - Slide 3 (35s)**

 First major announcement: Rolldown.

  It's Vite's new bundler, replacing Rollup. Complete rewrite in Rust for max performance.

  So how's the migration happening? Well, today Vite still uses Rollup. Then in June this year, Vite 7 came out with Rolldown as an experimental option. And next year in Q1, Vite 8 will make it the default.

  The performance gains? Massive. Let me show you.
-->

---
layout: full
---

<div class="flex items-center justify-center h-full">
  <div class="w-full max-w-6xl px-16">
    <h2 class="text-center">Benchmark on DT_Main (build time)</h2>
    <p class="opacity-50 text-center">On a M4 computer</p>
    <div class="flex justify-center items-center gap-16">
      <div class="flex flex-col items-center">
        <div class="w-32 h-32 rounded-full border-2 border-red-500 mb-6 relative z-10">
          <div class="w-full h-full rounded-full flex items-center justify-center" style="background: linear-gradient(rgba(239, 68, 68, 0.2), rgba(239, 68, 68, 0.2)), #0f0f0f;">
            <img src="./public/assets/rollup-logo.svg" width="64" />
          </div>
        </div>
        <h3 class="text-xl font-bold text-red-400 mb-3">Rollup</h3>
        <div class="text-5xl font-bold opacity-80">
          1:24
        </div>
        <p class="text-sm opacity-50 mt-2">minutes</p>
      </div>
      <div v-click="1" class="text-6xl opacity-40">
        →
      </div>
      <div v-click="1" class="flex flex-col items-center">
        <div class="w-32 h-32 rounded-full border-3 border-yellow-400 mb-6 relative z-10 shadow-lg shadow-yellow-500/40">
          <div class="w-full h-full rounded-full flex items-center justify-center" style="background: linear-gradient(rgba(234, 179, 8, 0.25), rgba(234, 179, 8, 0.25)), #0f0f0f;">
            <img src="./public/assets/lightning-down.svg" width="72" />
          </div>
        </div>
        <h3 class="text-2xl font-bold text-yellow-400 mb-3">Rolldown</h3>
        <div class="text-5xl font-bold bg-gradient-to-r from-orange-400 to-yellow-400 bg-clip-text text-transparent animate-pulse">
          8s
        </div>
        <p class="text-sm opacity-60 mt-2 font-semibold">seconds</p>
      </div>
    </div>
  </div>
</div>

<!--
**SPEAKER NOTES - Slide 4 (20s)**

This benchmark was done on our codebase.

  Rollup took 1 minute 24 seconds.
  Rolldown? 8 seconds.

  Let me show you the impact.
-->

---
layout: center
class: text-center
preload: false
---

<div class="flex items-center justify-center h-full">
  <div>
    <AnimateNumber v-slot="{ number, target }" :value="90.5" :duration="1000">
      <div
        class="text-9xl font-mono font-bold bg-gradient-to-r from-orange-400 to-yellow-400 bg-clip-text text-transparent"
        :style="{ transform: `scale(${1 + (number / target / 5)})` }"
      >
        {{ number.toFixed(1) }}%
      </div>
    </AnimateNumber>
    <p class="text-3xl opacity-100 !mt-18">Less moulining than before</p>
  </div>
</div>

<!--
**SPEAKER NOTES - Slide 5 (20s)**

That's 90% faster. A minute down to 8 seconds.

  What does that mean? CI runs faster. Less waiting. And you probably save a polar bear with each build!

  Not sure about the last one, but it's pretty cool anyway.

  Now, let's talk about the next big thing!
-->
---
layout: full
preload: false
---
<PulseGradient />
<div class="flex items-center justify-center h-full">
  <div class="text-center">
    <div class="mb-8">
      <img src="./public/assets/vite+.svg" class="h-48 mx-auto" />
    </div>
    <p class="text-xl opacity-70 font-bold !mt-10">
      The Unified JavaScript Toolchain
    </p>
  </div>
</div>

<!--
**SPEAKER NOTES - Slide 5bis (25s)**

  VitePlus.

  It unifies all our JavaScript dev tools into a single toolchain.

  Today we juggle multiple tools: Vite, ESLint, Prettier, Vitest... Each with its own config.

  VitePlus brings it all together. Let me show you.
-->

---
layout: full
---

<IframeSlide url="https://viteplus.dev/#feature-dev-build" />

<!--
**SPEAKER NOTES - Slide 6 (45s)**

  Here's the VitePlus documentation.

  [Browse the page briefly]

  So what does it unify?
  Build with Rolldown.
  Testing with Vitest.
  Linting with OxLint.
  Formatting with OxFmt. This one's still in development and should be available soon.
  And monorepo task running with intelligent caching. No config needed, it just works.
  

  One tool, one config. 10 to 100 times faster.

  It's free for open source and individuals. But for companies, well, you guessed it: not free. Evan hasn't shared pricing details yet though.
-->

---
layout: center
class: text-center
---

<h2 class="text-center mt--12">Benchmark on DT_Main</h2>
<p class="opacity-50 text-center">On a M4 computer</p>

<div class="mt-12 grid grid-cols-2 gap-16 max-w-4xl mx-auto">

<div>
<p class="text-sm opacity-60 uppercase tracking-wider mb-4">ESLint</p>
<div class="text-7xl font-bold opacity-40">
48.3s
</div>
</div>

<div v-click="1">
<p class="text-sm opacity-60 uppercase tracking-wider mb-4">OxLint</p>
<div class="text-7xl font-bold bg-gradient-to-r from-green-400 to-yellow-400 bg-clip-text text-transparent">
3.2s
</div>
</div>

</div>

<!--
**SPEAKER NOTES - Slide 6bis (30s)**

  Now let's dive into OxLint. I tested it on our code.

  Results:
  ESLint: 48 seconds.
  OxLint: 3 seconds.

  That's impressive, right? But actually, it's kind of cheating! OxLint can't parse everything in Vue files at the moment, and it has fewer rules than ESLint. But all these things will be fixed. 
  
  OxLint will probably become the default linter pretty soon.
-->

---
layout: full
---

<div class="flex items-center justify-center h-full px-16">
  <div class="grid grid-cols-3 gap-16 items-center w-full max-w-6xl">
    <div class="space-y-8 col-span-2">
      <h2 class="text-4xl font-bold mb-8">Vitest Browser Mode</h2>
      <div class="space-y-4">
        <div class="flex items-start gap-4">
          <div class="text-3xl">🎉</div>
          <div>
            <h3 class="text-xl font-bold text-green-400 mb-2">Browser Mode is Stable</h3>
            <p class="text-base opacity-80">Test in real browsers, no more JSDOM needed.</p>
          </div>
        </div>
      </div>
      <div class="space-y-4">
        <div class="flex items-start gap-4">
          <div class="text-3xl">🔍</div>
          <div>
            <h3 class="text-xl font-bold text-blue-400 mb-2">Visual Regression Testing</h3>
            <p class="text-base opacity-80">Visually compare your components, built-in natively in Browser Mode.</p>
          </div>
        </div>
      </div>
      <div class="space-y-4">
        <div class="flex items-start gap-4">
          <div class="text-3xl">🎭</div>
          <div>
            <h3 class="text-xl font-bold text-purple-400 mb-2">Playwright Traces Support</h3>
            <p class="text-base opacity-80">Advanced debugging with Playwright traces to easily diagnose failures.</p>
          </div>
        </div>
      </div>
    </div>
    <div class="flex items-center justify-center scale-150 mt--50">
      <img src="/assets/vitest-browser.png" class="w-full rounded-lg shadow-2xl" alt="Vitest Browser Mode" />
    </div>

  </div>
</div>

<!--
**SPEAKER NOTES - Slide 8 (35s)**

  Another major announcement: Vitest Browser Mode is now stable.

  Full disclosure: I haven't tested this yet. But here are the key features.

  First: Browser Mode is stable with Vitest 4 released in October. You can now test in real browsers.

  Second: Visual Regression Testing built-in. You can visually compare components to detect unwanted changes. By the way, shoutout to our QA team — they've already built something similar with Python for our design system, and it's been working great.

  Third: Playwright Traces support. When a test fails, you get complete traces to understand what happened.

  Pretty cool stuff for front-end testing.
-->

---
layout: full 
class: text-center
---

Key Takeaways
<div class="grid grid-cols-2 gap-8 mt-12 max-w-6xl mx-auto text-left">
  <div class="p-6 bg-gray-800 bg-opacity-10 rounded-xl border-l-4 border-violet-400 flex flex-col justify-center">
    <h3 class="text-2xl font-bold mb-3 text-violet-300">🚀 Rolldown & VitePlus</h3>
    <p class="text-lg opacity-90">The JavaScript ecosystem powered by Rust: <strong class="text-orange-300">-90% build time</strong> and a unified toolchain.</p>
  </div>
  <div class="p-6 bg-gray-800 bg-opacity-10 rounded-xl border-l-4 border-yellow-400 flex flex-col justify-center">
    <h3 class="text-2xl font-bold mb-3 text-yellow-300">⚡️ OxLint & OxFmt</h3>
    <p class="text-lg opacity-90">Linting and formatting <strong class="text-green-300">41x faster</strong> for instant feedback and improved DX.</p>
  </div>
  <div class="p-6 bg-gray-800 bg-opacity-10 rounded-xl border-l-4 border-green-400 flex flex-col justify-center">
    <h3 class="text-2xl font-bold mb-3 text-green-300">✅ Vitest Browser Mode</h3>
    <p class="text-lg opacity-90">Testing in real browsers, visual regression testing, and Playwright traces for increased reliability.</p>
  </div>
</div>

<!-- <div v-click="4" class="mt-16 text-sm opacity-50"> -->
<!-- Questions? -->
<!-- </div> -->

<!--
**SPEAKER NOTES - Slide 8bis (25s)**

  So, quick recap:

  Rolldown: Vite's new core in Rust. 90% faster builds. Released in June.

  VitePlus: One tool for everything. Up to 100 times faster. Coming soon.

  What does this mean for us? We'll migrate step by step. We've already seen the gains on our codebase. It's going to make our dev workflow way smoother.

  So yeah, JavaScript tooling is getting a massive performance boost thanks to Rust.

  Thanks for listening!
-->
