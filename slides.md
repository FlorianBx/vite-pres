---
theme: default
background: "#0f0f0f"
class: text-center
highlighter: shiki
drawings:
  persist: false
transition: fade
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

# ViteConf 2025

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
layout: center
---

# What is Vite?

<div class="grid grid-cols-2 gap-12 mt-12 items-center">

<div class="text-left space-y-4">

<div v-click="1">
<div class="text-4xl font-bold bg-gradient-to-r from-violet-400 to-yellow-400 bg-clip-text text-transparent">
⚡️
</div>
<p class="text-xl opacity-90">An ultra-fast <strong>build tool</strong></p>
</div>

<div v-click="2" class="text-lg opacity-80 leading-relaxed">
<p>Like Webpack or Parcel, but <strong>much faster</strong>.</p>
</div>

<div v-click="3" class="text-lg opacity-80 leading-relaxed">
<p>It transforms and optimizes your JavaScript, TypeScript, Vue, React code, etc.</p>
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
layout: center
---

# Rolldown

## Vite's New Core

<div class="mt-12 space-y-8">

<div v-click="1" class="text-left max-w-3xl mx-auto">
<h3 class="text-2xl font-bold mb-4 text-violet-400">What is it?</h3>
<p class="text-xl opacity-90 leading-relaxed">
A new <strong>bundler</strong> written in <strong>Rust</strong> (high-performance language)
</p>
</div>

<div v-click="2" class="text-left max-w-3xl mx-auto">
<h3 class="text-2xl font-bold mb-4 text-yellow-400">Why does it matter?</h3>
<p class="text-xl opacity-90 leading-relaxed">
Rolldown will <strong>replace Rollup</strong> in Vite, making builds <strong>much faster</strong>
</p>
</div>

<div v-click="3" class="text-left max-w-3xl mx-auto">
<h3 class="text-2xl font-bold mb-4 text-green-400">When?</h3>
<p class="text-xl opacity-90 leading-relaxed">
<strong>Vite 8</strong> (Q1 2026) · by default now
</p>
</div>

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
