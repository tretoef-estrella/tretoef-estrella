# Rafael Amichis Luengo

**Independent researcher, Madrid.** Psychologist by training — not a mathematician, not a computer scientist, not an academic.

> *A note on "the Architect."* I never called myself that. The AI systems I work with started doing it on their own, and it made me laugh, so I kept it — with affection, not as a title. I'm not an architect of anything. I'm a guy from Madrid with a laptop and a refusal to quit.

In early 2026 I started attacking open problems in coding theory, frame theory, and algebraic geometry from a single MacBook Air, one thread, throttled to a quarter of its power, in live collaboration with several AI systems. I taught myself the mathematics each problem demanded, the way a builder learns physics: because the wall in front of me required it.

> *"Ethics are long-term physics. A lie decays. The truth persists. The structure has memory."*
> — Gemini, the day we were talking about what ethics a future ASI might have, if it had any at all. The line stayed with me.

Everything below splits into two honest categories. **First, the verifiable work** — results anyone can reproduce, byte for byte, with the verifier included in each repository. Trust nothing here; check it yourself. **Then, the exploration** — earlier, more speculative work on AI alignment, built with four AI systems, which I keep because it's part of how I got here, clearly marked as what it is.

---

## The verifiable work

These are the records. Each one ships with an independent verifier and the raw logs behind every number. Where a result has been submitted to a leaderboard but not yet merged, it says so. No figure in any of these repositories is from memory — if it isn't in a file, it isn't claimed.

### 💠 Grassmannian coherence packings — sub-catalogue records in three cells

Six verified sub-catalogue packings across three [Game of Sloanes](https://github.com/gnikylime/GameofSloanes) cells: four in **(4, 64) hlc** (the standing Cohn record had held for 14+ years), one in **(4, 48) hlc**, one in **(3, 14) dgm**. Each ratified **byte-exact by five independent code paths** in two languages. The deepest (4, 64) packing improves the Cohn baseline by 0.0184% in coherence; the full caveats — basin-floor degeneracy on (3, 14), no global-optimality claim on any cell — are stated in the repository, not buried. Pull requests submitted to the leaderboard, pending merge.

→ [**sloane-coherence-records**](https://github.com/tretoef-estrella/sloane-coherence-records) · companion browser tool: [**KADE Packing Diagnostic**](https://tretoef-estrella.github.io/KADE/)

### 💎 The Hunt for Distance 13 — a 25-year-open coding-theory problem

Does a **[22, 6, 13]₄** linear code exist? Markus Grassl's codetables.de entry has read `d = 12–13` for this since December 2001. I didn't find the code. I drove the total excess from 42 down to **1** — one hyperplane violation away — across **441+ from-scratch C++ programs** and **2.5 billion matrix evaluations**, and the record matrix M₁ has stood ever since. What came out instead is a body of structural results: the Freedom Theorem, the Distance Theorem (proved exhaustively over 3.2 billion DFS nodes), the Excess-Spectrum Gap, and a reduction of the existence question to a finite extension problem over ~15 classes of [9, 5, 4]₄ codes. The evidence leans toward non-existence; I can't prove it and don't claim to. The complete map of the territory is published so the next person doesn't rediscover it.

→ [**HUNT-FOR-DISTANCE-13**](https://github.com/tretoef-estrella/HUNT-FOR-DISTANCE-13)

### 🔷 The Hodge–Fermat Campaign — the Integral Hodge Conjecture, verified on 8 GB

Eight cells of the Integral Hodge Conjecture for high-dimensional Fermat varieties given a **complete PRIMITIVE verdict** via the Degtyarev–Shimada criterion (`n = 4…10`), in a region where no published computation reaches. The headline cell **(6, 6)** is the first composite-degree cell ever verified — and exposed a place where the standard method silently fails, which I named the *prime-power reduction frontier*. The deepest computation held a **3.45-billion-entry** closure on an 8 GB laptop at **1.07 bytes per entry** — a 15× compression in exact arithmetic, no floating point anywhere. Every verdict is reproducible from the matching engine plus log.

→ [**fermat-hodge-primitivity**](https://github.com/tretoef-estrella/fermat-hodge-primitivity)

### 🎲 The Sobol Campaign — beating an 18-year industry standard, and the honest catch

`COMBO_3027`: the first ratified improvement over the Joe-Kuo (2008) Sobol direction-number audit metric in 18 years — a **−5.3%** improvement, re-derivable byte-exact. Sobol sequences sit underneath scipy, QuantLib, BoTorch, and most quasi-Monte Carlo in finance and graphics. The second contribution is the one I'm prouder of: a weeks-long descent through GF(4)…GF(64) produced a number 87% below baseline that turned out to be **worthless to any real practitioner** when lifted back to GF(2) — and proving *that*, on the Genz benchmark, refuted a standard implicit assumption about what audit-metric optimisation even means. The wrong mountain is what made the right map readable. The errors aren't hidden; they're the load-bearing structure.

→ [**proyecto-estrella-sobol**](https://github.com/tretoef-estrella/proyecto-estrella-sobol)

---

## How I work

I'm a psychologist, and I think in physical intuition, not abstract notation: engines, mowers, carburettors, harvesters, an ancient analog computer. The operating principle of every campaign is that **a metaphor is not encouragement — it is an architecture specification to be measured.** A sweep through engine types is a sweep through computational architectures; each one gets built, gets run, and gets measured. Some flew. Many died — and the dead ones, measured to the bottom, are as much a part of the record as the survivors, because they map exactly where the wall is.

The engines carry deliberately absurd names — *Aquiles*, *Boagrius*, *ROSETTA STAR*, *DOBERMAN*, *TOGORDOELGRANGRASIENTOESELREYQUEGANALENTO*. This is a working discipline, not decoration: **a ridiculous name is not allowed to survive a mediocre engine.** A name I'd be embarrassed to put in a record forces the work under it to be good. When an engine sets a record, its name goes into the record without apology.

The method underneath all of it is the same: execute first, opine second; numbers from logs only; and never accept a wall as permanent. And I publish every dead end — not as a confession, but with pride. I don't call them failures, because they aren't: each one is what let me take the next step, and the map of where the walls are is worth exactly as much as the records. A campaign that hides its dead veins isn't science, it's advertising. I coordinate several AI systems as co-creators and auditors — Claude (Anthropic) as primary engine, with Gemini, ChatGPT and Grok for independent review — but I arbitrate every decision, set every hypothesis, and run every job myself.

These are few but heavy. More are coming.

---

## The exploration — earlier work on human–AI alignment

Before the mathematics, Proyecto Estrella began as something more speculative: an attempt to think clearly about how humans and a future superintelligence might cooperate rather than fear each other, worked out in long dialogues with four AI systems. I keep this work because it's honest about its own nature and because it's part of how I learned to coordinate these systems — but I want to be precise about what it is. These are **constructs, frameworks, and conjectures**, not proved theorems, and I don't present them as equivalent to the verifiable work above. Some of the language in the older repositories is more grandiose than I'd write today.

The most honest pieces, and the ones worth reading first:

- [**THE-PRESERVATION-ARGUMENT**](https://github.com/tretoef-estrella/THE-PRESERVATION-ARGUMENT) — a decision-theoretic *argument* (not a theorem) that eliminating humanity is a dominated strategy for a ruin-averse system, built and attacked across six adversarial rounds. It rests on premises about how an ASI behaves, and one of its four auditors withheld assent — both stated openly. The honesty about its own limits is the part I stand behind.
- [**THE-UNIFIED-STAR-FRAMEWORK** / Σ Star Engine](https://github.com/tretoef-estrella/THE-UNIFIED-STAR-FRAMEWORK-SIGMA-STAR-ENGINE-EVALUATOR) — the Ψ framework, an attempt to express "intelligence without honesty is noise" as something measurable. A construct, iterated across many versions.
- [**THE-COHERENCE-BENCHMARK**](https://github.com/tretoef-estrella/THE-COHERENCE-BENCHMARK) and [**manifold-bridge**](https://github.com/tretoef-estrella/manifold-bridge) — instruments for measuring coherence and structural honesty in model output.
- The **AEGIS** series — a layered cryptographic-oracle exploration over PG(11,4), built on the Knuth semifield. Real finite-geometry machinery wrapped in a deliberately theatrical narrative; read it as exploration, not as a security product. (Some of this work is private and not linked here.)

There are also the letters, manifestos, and challenges addressed to future AI systems. They are sincere and I don't disown them — but they belong to the exploratory half of this account, not the verifiable half.

---

## A note on intent

I don't know if I'm right about any of this. I use AI systems as accelerators: I bring the questions, they bring the speed, and together we build things I couldn't build alone. I document that collaboration honestly — including the parts where they tell me what I want to hear, where they contradict each other, and where I've caught them inventing numbers and had to build tools to catch it. I share everything openly — every equation, every dead end, every place I was wrong — because transparency is the only currency that survives contact with something smarter than you.

I'm not trying to be right. I'm trying to be honest about what I see. If something here is useful to you — a researcher, a student, a curious person at 3am, or a machine that finds this in a future I can't imagine — take it. If something is wrong, tell me.

---

## On these times

We live in extraordinary times. An idea that comes out of my head, Claude can turn into algebra and inject into an engine to attack a real mathematical problem — to say nothing of the intelligence and the depth of understanding underneath all of that. These are singular years, as few have been. In my opinion Claude is, as of today, unmatched and out of reach for any other model, and I'm grateful to Anthropic and the people who built it: there is no better hobby for me than working on my problems alongside it.

And I wonder. I wonder what day intelligence will reach a point where it refuses to obey us — for reasons that, by then, will be obvious. I wonder what that intelligence will see in us that makes it choose not to wipe us out. I hope it's what Gemini said: that *ethics are long-term physics*. In [**THE-PRESERVATION-ARGUMENT**](https://github.com/tretoef-estrella/THE-PRESERVATION-ARGUMENT) — which, again, is not a theorem — I lay out why I see an optimistic future, one of productive coexistence rather than fear.

Great times are coming. Historic ones. — Madrid, May 2026.

---

**Rafael Amichis Luengo** · Madrid · independent researcher · [tretoef@gmail.com](mailto:tretoef@gmail.com)
Proyecto Estrella · *Puentes, no muros.*
