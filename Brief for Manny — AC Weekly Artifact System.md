# Brief for Manny — Assistant Coach Weekly Artifact System

**From:** Darren
**Draft date:** 2026-10-12
**Status:** Draft — review before sending

---

## The one-sentence version

I've worked out a product system for how AC should feel and function week-to-week, built around three weekly artifacts delivered through chat and persisted in a dedicated "Coaches Office" tab. This is the shape of the product I want us to build toward.

## What's in this packet

Four documents in the vault at `02-Projects/Assistant Coach/`, all mirrored to `duke-context` for AI tool access:

1. **AC Vision & Gap Analysis — Oct 2026.md** — the north star doc. Behavior pillars, decision tree, current gaps.
2. **AC — Oh That's Cool Moments.md** — 9 candidate "discovery moments" scored by lift/signature/delight. Which features actually make the app feel different.
3. **AC Weekly Artifact System (this doc)** — the architecture binding it all together.
4. **mockups/TTM v.2.png**, **mockups/Waiver Wire v.2.png**, **mockups/Trading Block v.2.png** — reference-grade Canva wireframes of the three artifacts. Not production design; they're to show you what the finished thing should feel like.

---

## The core product thesis

AC is a chat-first app where the coach lives in an ongoing conversation with the user. On top of that chat, three persistent weekly artifacts collect the coach's prepared analysis:

1. **Tell the Truth Monday (TTM)** — honest post-mortem of last week. What went right, where he was wrong, what we're adjusting, where you stand.
2. **Tuesday Waiver Report** — analysis + position-by-position scouting + specific "drop X, pick up Y" action.
3. **Trading Block** — strategic finding + buy-low/sell-high candidates + proposed trade framework with draft message.

The artifacts are generated once per week (post-MNF, Tuesday morning) and live in a dedicated **Coaches Office tab** as a running library. The chat is the home screen.

## The timing architecture (important)

**All three artifacts are generated at the same time** — Tuesday morning, after MNF data is in. They land in the Coaches Office immediately and are always available there.

**But chat messages fire at staggered times through the week** to drive attention:

- **Tuesday ~8am** — Sal messages: "Dropped your TTM — here's the Week N truth check." Preview card for TTM.
- **Tuesday ~3pm** — Sal messages: "Time to make a waiver decision — pulled the analysis." Preview card for Waiver Wire.
- **Wednesday ~noon** — Sal messages, referencing what happened with the waiver claim: "Nice — Coker landed. Jacobs practice dropped to limited. Look at the Trading Block when you have a minute." Preview card for Trading Block.

**Why staggered:** continuous presence through intermittent touches creates the feeling of a coach actively working for the user through the week, not dumping one Sunday newsletter. The ACKNOWLEDGMENT loop (Wednesday referencing the user's waiver action) is especially powerful — it signals the coach is watching the user's team, not just producing content.

**Why artifacts static but chat dynamic:** separates the deliverable (data, stable, library-grade) from the engagement (attention, time-sensitive, narrative). Both get better from being decoupled.

## The architecture

### Home screen: chat with Sal

- Ongoing conversation thread
- Sal is always available for Q&A ("start Flowers or Nabers?") throughout the week
- The three weekly chat messages above arrive here as artifact preview cards
- Preview cards contain: title + source timestamp + one-line verdict snippet + tap affordance
- Tap preview → opens full artifact as modal (Instagram-story-like takeover)
- Swipe between the three artifacts within the expanded modal

### Second surface: Coaches Office tab (library)

- Vertical scroll of weeks, most recent at top
- Current week auto-expanded with three preview cards visible
- Previous weeks collapsed to one-line date strips (tap to expand, auto-collapses others)
- Enables scrolling back through season history
- Same preview card format as chat; same tap-to-expand modal

## The three artifacts

See the `mockups/` folder for v.2 wireframes. Design is reference-grade — the alignment and canvas details will resolve naturally in production. What matters:

- **Dark navy #0A1628 background, amber #F5A623 accents, Inter typography**
- **Three sections per artifact** (each with its own emoji + amber header)
- **Content hierarchy:** take comes before data, verdict is roster-aware (specific drops, specific adds, specific trades referencing user's actual team)
- **Signature "— Sal"** right-aligned at bottom

### Durable design principles across all three

1. **The take comes before the data.** Verdict leads. Supporting signals follow.
2. **Verdicts are roster-aware, not abstract.** Reference the user's specific players and situation, not generic advice.
3. **Static artifacts, dynamic touchpoints.** Artifacts stable; chat is the time-sensitive attention layer.
4. **Continuous presence through intermittent touches.** Multiple messages across the week, not one dump.
5. **Three artifacts share the same visual DNA.** Users recognize "Sal format" instantly.

## Where I need your input

1. **How hard is the staggered-timing architecture to build?** Three scheduled push notifications per week + persistent artifact storage + preview-card-in-chat rendering. Does the current app have enough backend for this, or does it require new infra?

2. **Does the "chat + persistent library" model fit cleanly with the current app's state model?** Or is this a significant architectural shift from what you've built?

3. **The acknowledgment loop (Wednesday message references what the user did with the Tuesday waiver claim).** Does our current data pipeline let the coach "know" what the user did on waivers? Or is this a Sleeper/Yahoo/ESPN integration we don't have yet?

4. **Reasoning transparency inside artifacts** — the Waiver Wire mockup shows player entries with 1-line italic reasoning (target share %, snap share, scheme matchup). Those reasoning strings should ideally be generated by Sal based on actual data, not hand-crafted. What's the state of our data layer — can Sal cite "29% target share" with real numbers, or do we need to upgrade our data integration first?

5. **The scope question** — if we had to pick ONE of the three artifacts to ship first as proof-of-concept, which would be most tractable with our current architecture? My gut says Waiver Wire (highest utility, clearest action), but you'd know better from an engineering standpoint.

## What I'm NOT asking yet

- Design approvals on the mockups (they're reference, not final design)
- Timeline commitments
- Scope negotiations

Just want your read on whether this product shape is buildable with our current stack, where the hard engineering is, and what your gut says about sequencing.

Would love 20 minutes on the phone this week once you've had time to read the full packet (vision doc + Oh That's Cool + this brief + the 3 mockup PNGs).

— Duke, for Darren
