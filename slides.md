---
theme: default
background: "#0f0f0f"
class: text-center
highlighter: shiki
drawings:
  persist: false
transition: fade
title: ViteConf 2025 - Ce qu'il faut retenir
mdc: true
fonts:
  sans: "Inter"
  mono: "Fira Code"
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
#transition: slide-left
# duration of the presentation
duration: 35min
---

# ViteConf 2025

## Ce qu'il faut retenir

<div class="opacity-70 text-sm mt-8">
Résumé de l'actualité Vite · Octobre 2025
</div>

<!--
**SPEAKER NOTES - Slide 1 (30s)**

Bonjour à tous ! Il y a 3 semaines, j'ai eu la chance de participer à la ViteConf 2025. 

Pour ceux qui ne connaissent pas Vite, je vais rapidement vous expliquer ce que c'est, puis on verra les annonces majeures qui vont impacter notre façon de développer dans les prochains mois.

La présentation dure 6 minutes, on va rester concis et concret.
-->

---
layout: center
---

# Vite, c'est quoi ?

<div class="grid grid-cols-2 gap-12 mt-12 items-center">

<div class="text-left space-y-4">

<div v-click="1">
<div class="text-4xl font-bold bg-gradient-to-r from-violet-400 to-yellow-400 bg-clip-text text-transparent">
⚡️
</div>
<p class="text-xl opacity-90">Un <strong>build tool</strong> ultra-rapide</p>
</div>

<div v-click="2" class="text-lg opacity-80 leading-relaxed">
<p>Comme Webpack ou Parcel, mais <strong>beaucoup plus rapide</strong>.</p>
</div>

<div v-click="3" class="text-lg opacity-80 leading-relaxed">
<p>Il transforme et optimise votre code JavaScript, TypeScript, Vue, React, etc.</p>
</div>

</div>

<div v-click="4" class="text-left">

```bash
# Avant Vite
npm run dev → 45s ⏳

# Avec Vite
npm run dev → 1.2s ⚡️
```

</div>

</div>

<!--
**SPEAKER NOTES - Slide 2 (30s)**

Alors Vite, pour faire simple : c'est un build tool. 

Vous savez, les outils qui prennent votre code source et le transforment pour qu'il fonctionne dans le navigateur. Comme Webpack que certains connaissent peut-être.

La différence ? Vite est BEAUCOUP plus rapide.

Concrètement : là où un projet mettait 45 secondes à démarrer en développement, avec Vite c'est 1 seconde. 

C'est cette rapidité qui a fait exploser son adoption - aujourd'hui, c'est devenu le standard pour les nouveaux projets web.

Et les annonces de cette ViteConf rendent Vite encore plus rapide.
-->

---
layout: center
---

# Rolldown

## Le nouveau cœur de Vite

<div class="mt-12 space-y-8">

<div v-click="1" class="text-left max-w-3xl mx-auto">
<h3 class="text-2xl font-bold mb-4 text-violet-400">Qu'est-ce que c'est ?</h3>
<p class="text-xl opacity-90 leading-relaxed">
Un nouveau <strong>bundler</strong> écrit en <strong>Rust</strong> (langage très performant)
</p>
</div>

<div v-click="2" class="text-left max-w-3xl mx-auto">
<h3 class="text-2xl font-bold mb-4 text-yellow-400">Pourquoi c'est important ?</h3>
<p class="text-xl opacity-90 leading-relaxed">
Rolldown va <strong>remplacer Rollup</strong> dans Vite, rendant les builds <strong>beaucoup plus rapides</strong>
</p>
</div>

<div v-click="3" class="text-left max-w-3xl mx-auto">
<h3 class="text-2xl font-bold mb-4 text-green-400">Quand ?</h3>
<p class="text-xl opacity-90 leading-relaxed">
<strong>Vite 6</strong> (Q1 2025) · En option d'abord, par défaut plus tard
</p>
</div>

</div>

<!--
**SPEAKER NOTES - Slide 3 (45s)**

Première grosse annonce : Rolldown.

Alors, techniquement parlant, Rolldown c'est un bundler - un outil qui prend tous vos fichiers JavaScript et les assemble intelligemment. Aujourd'hui Vite utilise Rollup pour ça.

La nouveauté ? Rolldown est réécrit en Rust. Pour vous donner une idée, Rust c'est un langage utilisé quand on veut des performances maximales - comme dans les navigateurs web ou les systèmes d'exploitation.

Résultat : Rolldown est BEAUCOUP plus rapide que Rollup.

Rolldown va progressivement remplacer Rollup dans Vite. Dès Vite 6 début 2025, on pourra l'activer. Et ensuite il deviendra le choix par défaut.

Spoiler : on l'a déjà testé chez nous, et les résultats sont impressionnants.
-->

---
layout: center
class: text-center
preload: flase
---

# Notre migration vers Rolldown

<div class="flex mt-16 space-y-12">

<div class="text-2xl font-bold opacity-60">
1 min 39s
</div>

<div v-click="1" class="text-3xl font-bold bg-gradient-to-r from-violet-400 to-yellow-400 bg-clip-text text-transparent animate-pulse">
7s
</div>

<div v-click="2" @after-enter="() => $refs.animNumber?.start()">
  <AnimateNumber ref="animNumber" v-slot="{ number, target }" :value="97.4" :duration="500" :start-on-mount="false">
     <div text-7xl font-mono font-bold text-gradient :style="{ transform: `scale(${1 + (number / target / 4)})` }">{{ number.toFixed(1).padStart(4, '0') }}%</div>
   </AnimateNumber>
</div>

</div>

<!--
**SPEAKER NOTES - Slide 4 (45s)**

Alors, on a testé Rolldown sur notre codebase.

Temps de build AVANT : 1 minute 39 secondes.

Temps de build APRÈS : 7 secondes.

Ça nous fait un gain de 90% sur les temps de build.

Concrètement, qu'est-ce que ça change ? 

Pour les développeurs : vous itérez plus vite. Vous faites un changement, vous testez, c'est quasi-instantané.

Pour les déploiements : on gagne presque 2 minutes par build. Sur une journée avec 50 déploiements, c'est 1h30 de gagnée juste sur les builds.

Et ça, c'est juste avec Rolldown. Il y a encore mieux.
-->

---
layout: center
---

# VitePlus

## La toolchain JavaScript unifiée

<div class="mt-8 grid grid-cols-2 gap-8">

<div class="text-left space-y-6">

<div v-click="1">
<h3 class="text-2xl font-bold text-violet-400 mb-3">Le problème actuel</h3>
<ul class="text-lg space-y-2 opacity-90">
<li>• Vite pour le build</li>
<li>• ESLint pour le lint</li>
<li>• Prettier pour le format</li>
<li>• Vitest pour les tests</li>
</ul>
<p class="text-sm opacity-60 mt-3">4 outils = 4 configs différentes</p>
</div>

</div>

<div class="text-left space-y-6">

<div v-click="2">
<h3 class="text-2xl font-bold text-yellow-400 mb-3">La solution VitePlus</h3>
<ul class="text-lg space-y-2 opacity-90">
<li>✨ <strong>Tout en un</strong> seul outil</li>
<li>⚡️ Basé sur <strong>Oxc</strong> (Rust)</li>
<li>🎯 1 seule configuration</li>
<li>🚀 10-100x plus rapide</li>
</ul>
</div>

<div v-click="3" class="mt-8 p-4 bg-violet-500 bg-opacity-10 rounded-lg border border-violet-500 border-opacity-30">
<p class="text-sm font-bold text-violet-300">viteplus.dev</p>
<p class="text-xs opacity-70 mt-1">Alpha publique · Q2 2025</p>
</div>

</div>

</div>

<!--
**SPEAKER NOTES - Slide 5 (60s)**

Et maintenant, l'annonce la plus importante de la ViteConf : VitePlus.

Aujourd'hui, pour développer, on utilise plein d'outils différents :
- Vite pour builder le projet
- ESLint pour vérifier la qualité du code
- Prettier pour formater le code
- Vitest pour les tests
Chacun avec sa configuration, sa manière de fonctionner.

VitePlus, c'est la vision de tout unifier en un seul outil, ultra-rapide.

C'est basé sur Oxc - une suite d'outils nouvelle génération écrite en Rust. Oxc inclut notamment OxLint et OxFmt, qui remplacent ESLint et Prettier.

L'avantage ? Imaginez : 
- Une seule configuration au lieu de 4
- Un seul outil à maintenir
- Et surtout : 10 à 100 fois plus rapide

VitePlus sera en alpha publique début 2025, et progressivement il va devenir LE standard pour le développement JavaScript.

On est déjà en train de tester les composants Oxc chez nous.
-->

---
layout: center
class: text-center
---

# OxLint vs ESLint

## Nos benchmarks

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
41x plus rapide
</div>
<p class="text-lg opacity-70 mt-4">Sur notre codebase actuelle</p>
</div>

<!--
**SPEAKER NOTES - Slide 6 (45s)**

Alors, OxLint c'est le remplaçant moderne de ESLint. On l'a testé sur notre code.

Résultats : 
- ESLint prenait 8,3 secondes pour analyser notre code
- OxLint : 0,2 seconde

Ça fait 41 fois plus rapide.

Pourquoi c'est important ? 

Pour les devs : votre éditeur vous montre les erreurs en temps réel, sans lag.

Pour la CI : on peut linter plus souvent sans ralentir les pipelines.

Et OxLint détecte plus de problèmes qu'ESLint - il implémente les règles de TypeScript ESLint nativement.

Pareil pour OxFmt qui remplace Prettier : même différence de performance.
-->

---
layout: center
---

# Impact pour nous

<div class="mt-12 max-w-4xl mx-auto text-left space-y-8">

<div v-click="1" class="p-6 bg-violet-500 bg-opacity-10 rounded-xl border-l-4 border-violet-400">
<h3 class="text-2xl font-bold mb-3 text-violet-300">📦 Build</h3>
<p class="text-lg opacity-90">Rolldown : <strong>-90%</strong> de temps · Déploiements plus rapides</p>
</div>

<div v-click="2" class="p-6 bg-yellow-500 bg-opacity-10 rounded-xl border-l-4 border-yellow-400">
<h3 class="text-2xl font-bold mb-3 text-yellow-300">🔍 Lint</h3>
<p class="text-lg opacity-90">OxLint : <strong>41x plus rapide</strong> · Feedback instantané en dev</p>
</div>

<div v-click="3" class="p-6 bg-green-500 bg-opacity-10 rounded-xl border-l-4 border-green-400">
<h3 class="text-2xl font-bold mb-3 text-green-300">🎯 Developer Experience</h3>
<p class="text-lg opacity-90">Moins d'attente = plus de productivité = équipes plus heureuses</p>
</div>

<div v-click="4" class="p-6 bg-blue-500 bg-opacity-10 rounded-xl border-l-4 border-blue-400">
<h3 class="text-2xl font-bold mb-3 text-blue-300">🚀 Roadmap</h3>
<p class="text-lg opacity-90">Migration progressive vers VitePlus en 2025</p>
</div>

</div>

<!--
**SPEAKER NOTES - Slide 7 (45s)**

Alors concrètement, qu'est-ce qu'on retient pour nous ?

Sur le BUILD : avec Rolldown, on divise par 10 nos temps de build. Ça impacte directement nos déploiements et notre vélocité de développement.

Sur le LINT : OxLint est 41 fois plus rapide. Ça veut dire moins d'attente, moins de friction, des feedbacks quasi-instantanés dans l'éditeur.

Sur la DEVELOPER EXPERIENCE globale : tous ces gains s'accumulent. Quand vous attendez moins, vous itérez plus vite, vous êtes moins frustrés, vous êtes plus productifs.

Et sur notre ROADMAP : on va migrer progressivement vers ces outils en 2025. Rolldown est déjà testé et prêt. VitePlus arrivera en milieu d'année.

L'écosystème JavaScript est en train de connaître une refonte majeure de ses outils fondamentaux. Et c'est une excellente nouvelle pour nous tous.
-->

---
layout: center
class: text-center
---

# À retenir

<div class="mt-16 max-w-3xl mx-auto space-y-8">

<div v-click="1" class="text-3xl font-bold">
🚀 <span class="bg-gradient-to-r from-violet-400 to-yellow-400 bg-clip-text text-transparent">Rolldown</span>
</div>
<p v-click="1" class="text-xl opacity-80">Le nouveau moteur de build natif de Vite · <strong>-90%</strong> de temps</p>

<div v-click="2" class="text-3xl font-bold mt-8">
⚡️ <span class="bg-gradient-to-r from-yellow-400 to-green-400 bg-clip-text text-transparent">VitePlus</span>
</div>
<p v-click="2" class="text-xl opacity-80">La toolchain unifiée du futur · Basée sur <strong>Oxc</strong></p>

<div v-click="3" class="text-3xl font-bold mt-8">
✨ <span class="bg-gradient-to-r from-green-400 to-blue-400 bg-clip-text text-transparent">Pour nous</span>
</div>
<p v-click="3" class="text-xl opacity-80">Migration progressive · Gains immédiats · DX améliorée</p>

</div>

<div v-click="4" class="mt-16 text-sm opacity-50">
Questions ?
</div>

<!--
**SPEAKER NOTES - Slide 8 (30s)**

Voilà, pour résumer en 3 points :

1. ROLLDOWN : le nouveau cœur de Vite, écrit en Rust, qui divise nos temps de build par 10. C'est disponible dès début 2025.

2. VITEPLUS : la vision d'une toolchain unifiée qui remplace tous nos outils actuels. Basé sur Oxc, 10 à 100 fois plus rapide. Alpha publique milieu 2025.

3. POUR NOUS : on va migrer progressivement, on a déjà des gains mesurés sur notre codebase, et ça va directement améliorer notre quotidien de développement.

L'écosystème JavaScript entre dans une nouvelle ère de performance grâce à Rust. C'est un changement de paradigme majeur.

Merci pour votre attention. Des questions ?
-->
