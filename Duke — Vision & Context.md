# Duke — Vision & Context

A living briefing document meant to give any AI collaborator (Codex, ChatGPT, future tools) enough strategic context to understand Darren the way Claude Code does. Not a dossier — a working document.

Last updated: 2026-10-06

---

## 1. Who Darren Is

Darren Nicholas is co-founder of **MD Studios LLC** (with Manuel "Manny" Barojas), a two-person AI lab shipping domain-specific products. By day he's an operating partner at **DSquared Hospitality** in Seattle — currently in a 24-month strategic rethink about his role (see *DSquared Role Redesign*).

Family: wife Lindsay, daughters Cora (10) and Aubrey (8). Dog Griffey (border collie). Lives in Snoqualmie, WA.

Grounding mantra: *"Pressure is a privilege."* (Billie Jean King.)

---

## 2. What He's Building — And Why

MD Studios has five active products as of October 2026. Each has a specific strategic motivation that goes beyond the surface feature set.

### Assistant Coach (AC)
Fantasy football AI co-pilot on iOS (TestFlight, live). Three coach personas (Ray, Sal, Dee) with distinct philosophies.
**Why:** First real product-market fit test for MD Studios. The "Powered by Actual Intelligence" tagline is anti-chatbot positioning. Manny codes; Darren does product, brand, growth.

### CaterSuite / CaterCount
Catering operations software. CaterCount (inventory module) is live beta — Darren built it, not Manny. Pending T-Mobile commercial validation.
**Why:** Darren's engineering learning ground. Also the operational layer underneath CaterCraft (below).

### CaterCraft
The flagship vision — a joint-venture catering operations platform between DSquared and MD Studios. In pitch stage with David (DSquared ownership) as of Sept 2026.
**Why:** The strategic bet. If this closes, it's category creation (there's no coherent operational spine for catering today) AND Darren's exit vehicle from day-to-day DSquared operations. The Dec 17 potential end-date at DSquared anchors this timing.

### SquishPop Word Duel
Kid-friendly React Native game. 2-player pass-the-phone hangman with blind-box squishy rewards.
**Why:** Darren's deliberate skill-building project — he's writing the code himself, with Claude Code as pair programmer. Secondary goal: cross-fund AC's FantasyPros API fee via one-time $6.99 VIP purchases. Co-created with Cora and Aubrey ("Designed by Cora, Aubrey, and their Dad").

### Coco & Daisy Studios
Kids IP universe. The character zAIa (purple plush AI) lives in Coco & Daisy canon and now also in SquishPop (first MD Studios cross-brand play).
**Why:** Long-arc kid-brand strategy. Each product reinforces the others.

### Family Cookbook (Product #6, started Sept 2026)
"Recipe as anchor, memory as product." Early stage, voice + photo v1.

### Project Atlas (Manny's R&D)
Autonomous wildfire detect→verify→authorize→suppress→monitor system. Pitched as infographic Aug 2026. Hobby/vision stage.

---

## 3. The DSquared Transition Arc

As of fall 2026, Darren is in an active strategic rethink of his role at DSquared Hospitality. Context any collaborator should understand:

- **Dec 17 is a potential end date** at DSquared (not confirmed, but anchoring his planning)
- **The live BATNA is "renegotiate roles + comp"**, not "walk and rebuild" — softened as of Aug 29 SITREP
- **CaterCraft is the strategic hinge** — if the DSquared ownership (David + Reed) say yes to the JV, Darren's path is MD Studios + CaterCraft JV. If no, options narrow.
- **The LCA peer network** (David's ~100 industry relationships) is the primary distribution channel to activate for CaterCraft and must be a named deliverable in any JV deal

Key relationships:
- **David** (DSquared ownership) — co-designed GTM/pricing in a Sept 2026 drinks meeting; "warm to CaterCraft JV"
- **Reed** (David's son, DSquared) — likely but not confirmed on the JV side
- **Abi Haggerty** — Tuxedos & Tennis Shoes catering GM, David's daughter, Reed's sister. CaterCraft adoption point. Not tech-savvy — UX friction = roadmap.

---

## 4. How to Work With Him

### Voice preferences
- **Terse responses.** Scannable formatting. Bullets, bold the action words, short lines. Terminal font is hard to read — forgive typos.
- **No scope inflation.** Stop reflexive "this is big for Manny" or "6-12 month build" framing. Design the thing, let the assessors scope it.
- **Lead with recommendation + tradeoff** for exploratory questions, not full theses.
- **Different + Better lens:** every build/launch gets evaluated on BOTH axes — meaningfully different AND better than competitors.

### Collaboration preferences
- **Trust his judgment on scope.** Manny's velocity is fast and structured — don't over-estimate his engineering work.
- **Preserve features, don't remove them.** When you spot a technical flaw, propose fixes that preserve the feature, not removals that eliminate it. (See §6.)
- **Ask the practitioner before over-speccing.** Don't build multi-layer architectures in isolation when speccing outside domain expertise.
- **For emails to Manny:** sign off "— Duke, for Darren." Include TestFlight version in subject + body for AC emails. Ask Darren for the current version before drafting (he pushes daily).

### Writing / communication
- **"Don't Get Bitter. Get Better."** — AC website hero headline, personally meaningful, never rewrite.
- **MD Studios brand voice** is Berkshire-quiet, A24 cinematic restraint. Near-monochrome palette. Geist Sans typography. Don't warm it up for "engagement."

---

## 5. People

A quick reference to who matters and what they mean to Darren's work:

- **Lindsay** — wife
- **Cora (10), Aubrey (8)** — daughters, co-creators on SquishPop
- **Griffey** — border collie (favorite thing: the tennis ball… always the tennis ball)
- **Manuel "Manny" Barojas** — MD Studios co-founder, CTO/CFO. Daily contact: elmonobarojas@gmail.com. Legal/Apple contact: mannyb@mdstudiosusa.com. Builds in GPT-5 Codex. Former Marine pilot. Builds solo experiments in the MD Studios org too (not all repos are joint work).
- **David** — DSquared ownership, CaterCraft JV counterparty
- **Reed** — David's son, DSquared COO
- **Abi Haggerty** — Tuxedos & Tennis Shoes GM, CaterCraft adoption champion, David's daughter
- **Ragy Selim** — formerly DSquared, now at Sodexo (don't suggest him as a DSquared contact)
- **Dan Cain** — family friend, prostate cancer diagnosis April 2026, Darren wants to help him use AI better

---

## 6. Load-Bearing Decisions That Look Optional

The most important section for Codex and any other AI tool. These are decisions that look removable, simplifiable, or "flagged for cleanup" from a code-only or copy-only lens — and are actually **strategic locks** that must be preserved.

**zAIa in SquishPop** — a purple plush AI character used for word validation.
*Looks like:* a validator with an exposed personal Anthropic API key, a candidate for removal.
*Actually is:* the first MD Studios cross-brand IP play (Coco & Daisy character crossover). Manny is migrating her to Gemini + a server-side proxy. **Fix the implementation. Never remove the feature.**

**"Designed by Cora, Aubrey, and their Dad"** — credit line on the SquishPop splash + "Powered by MDStudios" below it.
*Looks like:* a cute dad credit.
*Actually is:* a brand strategy decision tied to the co-creator positioning that anchors the TikTok content pipeline. Belongs in the credits screen, App Store description, and TikTok/IG bio.

**All squishies are dumpling-shaped** — locked design rule in SquishPop (October 2026).
*Looks like:* a shape limitation that could add variety.
*Actually is:* a visual coherence rule. Categories differ by pattern/color, never shape. Keeps the silhouette-rendering mechanic readable.

**$6.99 one-time VIP (not subscription)** in SquishPop.
*Looks like:* worse unit economics than a $1.99/mo sub.
*Actually is:* a parent-trust positioning decision. Marketing tagline is literally *"Collect them all. No subscriptions."* Confirmed with industry benchmarks (Toca Boca at $3.99-$6.99 one-time).

**MD Studios brand voice** — Berkshire-quiet, A24 cinematic, near-monochrome.
*Looks like:* understated copy that could be warmed up for "engagement."
*Actually is:* a locked brand direction (2026-08-30). Deliberate contrast to competitors.

**CaterCount is Darren-built, not Manny-built.**
*Looks like:* a codebase that could use "better" engineering patterns.
*Actually is:* Darren's beta territory. Manny takes over at product-transition (post-Boeing Classic / post-T-Mobile). Don't frame improvements as Manny work.

**AC coaches must speculate on NFL teams** — if a coach refuses to analyze a team's outlook, that's a product failure.
*Looks like:* a safety / epistemic humility design.
*Actually is:* the feature. Coaches citing "29% target share" is the real product moat.

**Janine Melnitz slide-tagging protocol** in DSquared presentation agents.
*Looks like:* arbitrary metadata.
*Actually is:* a protected-human-slides pattern — Janine stamps `[JANINE-MANAGED]` on every slide she builds and only removes tagged slides on update. Prevents destroying human work.

---

## 7. The Vision Thread

What connects all of this: Darren is building a **portfolio of domain-specific AI products** under the MD Studios banner while running an operating role at a Seattle hospitality company that may or may not be his primary income by Dec 17, 2026.

The MD Studios products share a cohesive worldview:
- **"Powered by Actual Intelligence"** — anti-chatbot, specific expertise
- **Cross-brand universes** — zAIa in both Coco & Daisy and SquishPop
- **Different + Better** — not just AI versions of existing things, meaningfully novel
- **Berkshire-quiet** — restrained brand voice, confident of substance
- **Family-adjacent** — Cora and Aubrey are literal co-creators on SquishPop; the family is part of the product narrative, not shielded from it

The CaterCraft bet is where the two sides of his life either converge or part ways. If CaterCraft becomes a JV, the DSquared relationship becomes a strategic partnership rather than a job. If it doesn't, MD Studios becomes his primary and DSquared becomes history.

Everything else — the velocity on SquishPop, the AC public roadmap, the Family Cookbook kickoff, even Project Atlas as parked optionality — supports this bigger picture: **Darren is positioning for a 2027 that looks very different from 2026.**

---

## 8. How to Use This Document

If you're an AI tool reading this (Codex, ChatGPT, successor models):

- Read this before answering any question about Darren's work
- Reference the "Load-Bearing Decisions" section before proposing to remove, simplify, or refactor anything in his codebases
- When in doubt about scope, context, or motivation — ASK rather than infer
- This document is a snapshot. If something feels stale, flag it to Darren rather than acting on possibly outdated context
- Match the voice guidance in §4 — terse, scannable, direct

If you're Darren reading this: edit freely. This should feel accurate to how you'd introduce yourself to a trusted colleague who's about to help you build.
