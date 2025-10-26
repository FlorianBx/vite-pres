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

Hello everyone! Three weeks ago, I had the opportunity to attend ViteConf 2025.

For those unfamiliar with Vite, I'll quickly explain what it is, then we'll look at the major announcements that will impact how we develop in the coming months.

The presentation lasts 6 minutes, we'll keep it concise and concrete.
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
      <img class="rounded" src="data:image/png;base64,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" />
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

<div class="flex gap-4 scale-70 justify-end mt--8 mr--48">
<h2 class="">Rolldown</h2>
<img src="./public/assets/lightning-down.svg" width="20" />
</div>

<div class="mt-1 space-y-8">
<h3 class="text-2xl font-bold mb-4 text-violet-400">What is it?</h3>
<div class="flex justify-around">

<div v-click="1" class="text-left max-w-3xl">
<img src="./public/assets/rollup-logo.svg" width="120" />
</div>

<div v-click="2" class="text-left max-w-3xl mt--8 mx-auto">
<img v-click="4" src="./public/assets/Original_Ferris.svg" width="96" />
<Arrow width="6" color="orange" x1="300" y1="200" x2="700" y2="200" />
</div>

<div v-click="3" class="text-left max-w-3xl">
<img src="./public/assets/lightning-down.svg" width="120" />
</div>

</div>

<h3 class="text-2xl font-bold mb-4 text-green-400">When?</h3>
<p class="text-xl opacity-90 leading-relaxed">
<strong>Vite 8</strong> (Q1 2026) · by default now
</p>
</div>


<!--
**SPEAKER NOTES - Slide 3 (45s)**

First major announcement: Rolldown.

So, technically speaking, Rolldown is a bundler - a tool that takes all your JavaScript files and intelligently assembles them. Today Vite uses Rollup for this.

What's new? Rolldown is rewritten in Rust. To give you an idea, Rust is a language used when you want maximum performance - like in web browsers or operating systems.

Result: Rolldown is MUCH faster than Rollup.

Rolldown will progressively replace Rollup in Vite. Starting with Vite 6 in early 2025, we'll be able to enable it. And then it will become the default choice.

Spoiler: we've already tested it internally, and the results are impressive.
-->

---
layout: full
class: text-center
preload: flase
---

# Our Rolldown Migration

<div class="flex flex-col mt-16 space-y-12">

<div class="w-full flex justify-around gap-8 items-center">
<div class="text-6xl font-bold opacity-60">
1 min 39s
</div>

<div v-click="1" class="text-7xl font-bold bg-gradient-to-r from-violet-400 to-yellow-400 bg-clip-text text-transparent animate-pulse">
7s
</div>
</div>

<div v-click="2" class="mt-20">
 <template v-if="$clicks === 2">
  <AnimateNumber v-slot="{ number, target }" :value="97.4" :duration="500">
    <div 
        class="text-8xl font-mono font-bold text-gradient" 
        :style="{ transform: `scale(${1 + (number / target / 4)})` }"
    >
        {{ number.toFixed(1).padStart(4, '0') }}%
    </div>
   </AnimateNumber>
</template>
</div>

</div>

<!--
**SPEAKER NOTES - Slide 4 (45s)**

So, we tested Rolldown on our codebase.

Build time BEFORE: 1 minute 39 seconds.

Build time AFTER: 7 seconds.

That's a 90% improvement in build times.

Concretely, what does this change?

For developers: you iterate faster. You make a change, you test, it's almost instantaneous.

For deployments: we save almost 2 minutes per build. Over a day with 50 deployments, that's 1.5 hours saved just on builds.

And that's just with Rolldown. There's even better.
-->

---
layout: center
---

# VitePlus

## The Unified JavaScript Toolchain

<div class="mt-8 grid grid-cols-2 gap-8">

<div class="text-left space-y-6">

<div v-click="1">
<h3 class="text-2xl font-bold text-violet-400 mb-3">Current Problem</h3>
<ul class="text-lg space-y-2 opacity-90">
<li>• Vite for builds</li>
<li>• ESLint for linting</li>
<li>• Prettier for formatting</li>
<li>• Vitest for testing</li>
</ul>
<p class="text-sm opacity-60 mt-3">4 tools = 4 different configs</p>
</div>

</div>

<div class="text-left space-y-6">

<div v-click="2">
<h3 class="text-2xl font-bold text-yellow-400 mb-3">The VitePlus Solution</h3>
<ul class="text-lg space-y-2 opacity-90">
<li>✨ <strong>All-in-one</strong> tool</li>
<li>⚡️ Based on <strong>Oxc</strong> (Rust)</li>
<li>🎯 Single configuration</li>
<li>🚀 10-100x faster</li>
</ul>
</div>

<div v-click="3" class="mt-8 p-4 bg-violet-500 bg-opacity-10 rounded-lg border border-violet-500 border-opacity-30">
<p class="text-sm font-bold text-violet-300">viteplus.dev</p>
<p class="text-xs opacity-70 mt-1">Public alpha · Q2 2025</p>
</div>

</div>

</div>

<!--
**SPEAKER NOTES - Slide 5 (60s)**

And now, the most important announcement from ViteConf: VitePlus.

Today, for development, we use many different tools:
- Vite to build the project
- ESLint to check code quality
- Prettier to format code
- Vitest for tests
Each with its configuration and way of working.

VitePlus is the vision of unifying everything into a single, ultra-fast tool.

It's based on Oxc - a next-generation tooling suite written in Rust. Oxc includes notably OxLint and OxFmt, which replace ESLint and Prettier.

The advantage? Imagine:
- A single configuration instead of 4
- A single tool to maintain
- And most importantly: 10 to 100 times faster

VitePlus will be in public alpha early 2025, and progressively it will become THE standard for JavaScript development.

We're already testing Oxc components internally.
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
