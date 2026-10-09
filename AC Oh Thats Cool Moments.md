# Assistant Coach — "Oh, That's Cool" Moments

**Purpose:** A catalog of discovery moments in AC — the screens, features, and interactions where a user says *"oh, I didn't even know he did THAT."* The new toys that come with the new toy.

The guiding principle (via Darren's dad getting a car with a map screen for the first time): *"You know it's cool when your new toy comes with its own new toys."* Right now AC has zero of these. This document lists candidates.

Each moment is scored for:
- **Logic depth** — does the coaching reasoning hold up?
- **Delight** — does it make the user grin?
- **Lift** — how hard is it to build?
- **Signature** — does it brand AC specifically, or could any app do it?

Last updated: 2026-10-09
Status: Draft catalog for Darren + Manny discussion

---

## 1. The Hire Screen (Onboarding) 🏈

**The moment:** First time opening the app. User expects "pick an AI assistant." Gets something richer.

**What they see:** Not a list of three cards with names. Three distinct profiles — Ray, Sal, Dee — each with a one-sentence philosophy, a signature line about what they BELIEVE, and a small sample of how they'd handle a classic fantasy decision ("Start Flowers or Addison?"). User sees that each coach's answer is genuinely different. The hire isn't just a cosmetic choice; it's a philosophical commitment for the season.

**Why it feels cool:** User realizes they're not picking skin color on the same AI underneath. They're hiring a philosophy. This is the first *"oh, these actually ARE different"* moment.

**Logic / Delight / Lift / Signature:** 9 / 8 / 5 / 10 — this is uniquely AC.

**Visual direction:** Three profile cards. Same background but each coach has a distinct lighting and visual personality. Below each, a 2-line sample answer to the same question — side-by-side, so the differences are visible.

---

## 2. The Texted Recommendation 📱

**The moment:** User asks their first question. Response arrives.

**What they see:** Not a chat bubble with an AI icon. A styled text message interface — the kind you'd get from a real coach texting you. Timestamp. Confident, specific, cited. No "Great question!" preamble. No hedging.

> *"Start Flowers. Three reasons: 29% target share through 5 games. Opponent allowing 180 YPG to WRs ranked by DVOA. His pattern vs zone coverage = 1.2x his season average. Lock it in by Sunday 1pm."*

**Why it feels cool:** First recommendation lands and it doesn't feel like ChatGPT with a persona on top. It feels like your buddy who happens to be an elite analyst texted you back.

**Logic / Delight / Lift / Signature:** 8 / 10 / 3 / 8 — mostly a UI + prompt refinement.

**Visual direction:** iMessage-style thread. Grey user messages on left, coach messages on right in a color coded to his personality. No chat UI chrome. No "AI assistant" icons.

---

## 3. Tell the Truth Monday 📅

**The moment:** Monday morning after games. User opens the app with their weekly result still fresh.

**What they see:** A one-screen honest recap from the coach. Three sections:
- **What went right.** Specific. ("Jahmyr won you Week 5. 24.6 points. The matchup read I gave you Thursday was accurate.")
- **What went wrong.** Honest. ("Flowers was my worst call. I told you to start him and he did nothing. Here's what I missed: didn't weight the Baltimore secondary properly against zone looks.")
- **What we learned.** Forward-looking. ("Next week we trust volume + healthy coverage matchup more than I did this week. Noted.")

**Why it feels cool:** The coach is honest about his mistakes. Every other AI tool pretends it was right. This one owns the misses. It builds trust by being vulnerable — which paradoxically makes future recommendations MORE trustworthy.

**Logic / Delight / Lift / Signature:** 10 / 10 / 6 / 10 — this is the single biggest moat. No competitor does this. Also matches the "Don't Get Bitter. Get Better." brand headline exactly.

**Visual direction:** Clean, serious. Like a coach's post-game notes. Three sections stacked. Minimal color. Could use a small streak counter: "Last 10 recommendations: 7-3."

---

## 4. Tuesday Waiver Wire ⚡

**The moment:** 7am Tuesday. Push notification: *"3 moves to look at. Open when you've got a minute."*

**What they see:** The coach has already looked at the waiver wire for the user's specific team. Three prioritized recommendations:
- **Must claim.** The highest-conviction pick for their roster. Why.
- **Worth considering.** Context-dependent, requires user judgment.
- **Hold off.** A player everyone is chasing that the coach thinks is a trap.

Each has reasoning. Each has suggested FAAB bid or waiver priority order.

**Why it feels cool:** The user wakes up to work already done. Not "ask me about waivers" — the coach already analyzed their roster, scanned who's available, and prepared the morning briefing. Feels like having an analyst on retainer.

**Logic / Delight / Lift / Signature:** 10 / 10 / 7 / 10 — delivers on the "proactive, not reactive" vision pillar directly.

**Visual direction:** Three-card stack. Each card has the player, the reasoning, and a one-tap "add to waiver claim" action if we can integrate with Yahoo/Sleeper/ESPN APIs.

---

## 5. The Reasoning X-Ray 🔍

**The moment:** Any time the coach gives a recommendation, the user wonders "why that one over the alternative?"

**What they see:** Tap and hold on any recommendation → the screen flips to show the decision tree. Signals used, weights applied by this specific coach's philosophy, confidence level, what SIGNALS WOULD HAVE CHANGED THE ANSWER.

Example:
- Signal: Target share. Weight: 40%. Value: 29% (above threshold).
- Signal: Opponent DVOA. Weight: 25%. Value: 7th-worst (favorable).
- Signal: Trajectory. Weight: 20%. Value: trending up.
- Signal: Scheme matchup. Weight: 15%. Value: neutral.
- **Confidence: Medium-High.** Flip Signal 1 to <18% target share → recommendation would reverse.

**Why it feels cool:** Users get to look at the coach's homework. First time any fantasy tool has shown its work this way. Advanced users dive into the signals; casual users just appreciate the honesty.

**Logic / Delight / Lift / Signature:** 10 / 9 / 8 / 10 — this is the reasoning transparency moat made visible.

**Visual direction:** Clean data visualization. Think Apple Fitness rings but for signals. Each signal is a labeled bar; weighted bars add to recommendation. Minimal chrome.

---

## 6. Trade Finder 🤝

**The moment:** Mid-week, user is thinking about shaking up the roster.

**What they see:** A "Trade Finder" screen. The coach has already analyzed:
- Each other user in your league (if integrated) and what positions they're weak at
- Your own roster surpluses and needs
- Fair value trade frameworks that could benefit both sides

Three suggested trades, each with: who to approach, what to offer, what to ask for, and why both sides win. One-tap button: "Draft message to send them."

**Why it feels cool:** The coach is thinking about the entire LEAGUE, not just your team. Trade proposals usually feel one-sided or extortionate. These feel balanced because the coach is modeling fairness, not just maximizing you.

**Logic / Delight / Lift / Signature:** 9 / 9 / 9 / 10 — requires league-level data integration but has huge payoff. Signature AC feature.

**Visual direction:** Three horizontal cards. Each shows: "Approach Nick → Offer Flowers for his Jacobs. Here's why he says yes. Here's why you win." Expandable reasoning.

---

## 7. Sunday Morning Check ⏰

**The moment:** Sunday morning, 2 hours before kickoff. Push notification.

**What they see:** The coach's final-check briefing on the user's locked-in lineup. Three parts:
- **Confidence check.** "Your lineup grades out at B+. One concern — let's talk about Flowers."
- **Last-minute swap suggestion.** "If you want to pivot: swap Flowers for Nabers. Same upside, better matchup."
- **One thing to watch.** "Keep an eye on Jacobs's inactive list — his snap percentage last week was concerning."

**Why it feels cool:** The user feels like someone is in their corner right before game time. Not generic advice — specifically about THEIR lineup, right when they can still act.

**Logic / Delight / Lift / Signature:** 9 / 10 / 6 / 9 — proactivity + timeliness combined. Pure "ride-or-die coach" vibe.

**Visual direction:** Dashboard-style one-screen view. Lineup across top. Three callouts below. A countdown timer to kickoff.

---

## 8. The Season Report Card 📊

**The moment:** End of each month. Push notification.

**What they see:** A reflection the coach has prepared on the user's journey:
- **What you've gotten better at.** "You're asking better questions about matchup now. Three months ago you were asking about raw points."
- **Where I've been wrong.** "I overestimated opportunity volume vs. efficiency in Weeks 3-5. Adjusted since."
- **What I notice about your style.** "You're risk-averse. That's helped you avoid bust weeks, but you may be leaving ceiling on the table."
- **What we work on next month.** One specific habit.

**Why it feels cool:** The coach is TEACHING the user, not just answering questions. The product gets more valuable the longer you use it. This is the retention engine.

**Logic / Delight / Lift / Signature:** 10 / 9 / 7 / 10 — nobody does this.

**Visual direction:** Letter-style layout. Could literally look like a handwritten note from the coach. More intimate than data-heavy.

---

## 9. The Draft Day Companion 🎯

**The moment:** Live during the user's fantasy draft. Season starter.

**What they see:** A dedicated draft mode. The coach whispers in their ear every pick:
- "Ray would take Flowers here. 2nd round value based on his volume model."
- "Ray would hold. Wait for Round 4 — there's a TE run coming."
- "Ray's not loving this board for you. Pivot plan: punt RB2, grab elite WR."

Reactive, situational, drafted-against-the-board.

**Why it feels cool:** The user has a coach in their ear during the most important moment of the fantasy season. Every other tool is a draft board or ranker. This is a *coach present during the draft.*

**Logic / Delight / Lift / Signature:** 10 / 10 / 9 / 10 — this is a signature product.

**Visual direction:** Tight, dark UI designed for live use. Draft board visible, coach messages overlay. Short, punchy, read-at-a-glance.

---

## Ranking by "cool factor" + brand signature

Based on the four scores combined:

1. **Tell the Truth Monday** (10 / 10 / 6 / 10) — biggest brand moat, must-build
2. **Tuesday Waiver Wire** (10 / 10 / 7 / 10) — proactivity made real
3. **The Reasoning X-Ray** (10 / 9 / 8 / 10) — transparency moat visible
4. **Trade Finder** (9 / 9 / 9 / 10) — league-aware thinking
5. **The Draft Day Companion** (10 / 10 / 9 / 10) — signature product, highest lift
6. **The Season Report Card** (10 / 9 / 7 / 10) — retention engine
7. **The Hire Screen upgrade** (9 / 8 / 5 / 10) — fastest to ship
8. **The Texted Recommendation** (8 / 10 / 3 / 8) — mostly a UI refinement
9. **Sunday Morning Check** (9 / 10 / 6 / 9) — great quality-of-life win

---

## Which 2-3 to visualize first

My recommendation for which to prompt into Nano Banana / DALL-E for mockups:

- **#3 Tell the Truth Monday** — would make the strongest brand image. The "coach admitting mistakes" visual is deeply human.
- **#4 Tuesday Waiver Wire** — the clearest "I didn't even ask and he was already working" moment.
- **#5 The Reasoning X-Ray** — makes the invisible visible. If this UI is beautiful, it IS the pitch.

Alternative if you want one bigger cinematic piece: generate an image of all three screens shown as iPhones on a desk, with notifications arriving in sequence — Monday's truth bomb, Tuesday's waivers, Sunday's check. That one composition shows the weekly cadence.

---

## Image generation prompts (ready to paste)

### Tell the Truth Monday
```
A hyper-realistic iPhone 16 Pro screenshot, framed close-up with slight angle, 
warm morning light from the side. The screen shows a fantasy football app in 
dark mode. At the top: "Tell the Truth Monday · Week 5." Below in three sections:
"What went right — Jahmyr won you Week 5. 24.6 points." / "Where I was wrong — 
Flowers was my worst call. Here's what I missed: didn't weight Baltimore's zone 
coverage properly." / "What we learned — Next week we trust volume + healthy 
coverage matchups more." Clean dark UI, warm accent color (amber), Fredoka or 
Inter typography, a small coach avatar in the top corner. Mood: honest, serious, 
intimate. Shot like an Apple product photo. No fake stock-photo background — 
plain wooden desk, coffee mug slightly out of focus.
```

### Tuesday Waiver Wire
```
A hyper-realistic iPhone screenshot. The screen shows a fantasy football app with
3 stacked cards labeled "Tuesday Waiver Report · 7:03am." Card 1 (highlighted 
amber): "MUST CLAIM — Zay Flowers, WR, BAL. Season-high target share, favorable 
Week 6 matchup. Suggest 18% FAAB." Card 2: "WORTH CONSIDERING — Tyler Allgeier, 
RB, ATL. Backfield split shifting." Card 3 (muted): "HOLD OFF — Chase Brown. 
Everyone's chasing last week; the usage won't repeat." Each card has a short 
reasoning paragraph. Dark UI, amber accents, serious design feel. Clean 
Inter typography. Shot like Apple's App Store screenshots — just the phone, 
clean background.
```

### The Reasoning X-Ray
```
A hyper-realistic iPhone screenshot. The screen shows a fantasy football app in 
"reasoning view." A recommendation at top: "START ZAY FLOWERS." Below it, four 
horizontal weighted bars labeled: "Target Share · 40% weight · value 29% ✓" / 
"Opponent DVOA · 25% weight · rank 7th-worst ✓" / "Trajectory · 20% weight · 
trending up ✓" / "Scheme matchup · 15% weight · neutral." Below: "Confidence: 
Medium-High" and "If target share dropped below 18%, I'd flip the call." 
Clean data-forward UI, serious tone, like a trader's dashboard but minimalist. 
Dark mode, amber accents. Shot like Apple product photography.
```

---

## How this doc gets used

- **For Darren** → the catalog of "oh that's cool" moments to internalize the vision
- **For Manny** → a feature wishlist with "cool factor" and "lift" scores so he can see which deliver biggest brand impact for the engineering invested
- **For Codex** → architectural research — "which of these are low-lift wins I can ship before fantasy playoffs?"
- **For future product discussions** → a living backlog to add to as more "oh cool" moments are discovered through use + feedback

Add to this doc as new moments occur. Delete items that don't survive playtest. Edit scores as reality adjusts.
