# AC Weekly Artifact System — Build Spec

Build this next. Tight spec; strategic rationale lives in the companion docs listed at the bottom.

## What we're building

Three weekly artifacts in AC, delivered via chat + persisted in a new "Coaches Office" tab.

- **TTM (Tell the Truth Monday)** — Monday-slate post-mortem: what went right, where Sal was wrong, what we're adjusting, where you stand
- **Tuesday Waiver Report** — analysis paragraph + position-by-position scouting (2 players each) + specific "drop X, add Y" with FAAB bid
- **Trading Block** — strategic finding + sell high / buy low lists + proposed trade with draft message to counterparty

Reference mockups at `ac-mockups/` show the look and content shape.

## Architecture

### Home screen stays as the chat with Sal
- Sal is always available for ongoing Q&A
- Three artifact-notification messages fire from Sal at staggered times
- Each message carries a preview card: title + source timestamp + 1-line verdict
- Tap preview → full artifact opens as modal (Instagram-story-like), swipe between TTM / Waiver / Trading

### New "Coaches Office" tab = library
- Vertical scroll of weeks, most recent at top
- Current week auto-expanded with three preview cards visible
- Previous weeks collapsed to date strips, tap to expand (auto-collapses others)

### Timing architecture
- **All three artifacts generated at once Tuesday morning**, post-MNF, as soon as data settles
- They live in Coaches Office immediately, always available
- Chat notifications stagger to drive attention and create the "coach continuously working" feel:
  - **Tuesday ~8am** — TTM dropped
  - **Tuesday ~3pm** — Waiver Report ready, claim window open
  - **Wednesday ~noon** — Trading Block ready; message references what happened with the Tuesday waiver claim

## Locked design principles

1. **The take comes before the data.** Verdict leads every section.
2. **Verdicts are roster-aware.** Reference the user's actual players, not generic advice.
3. **Static artifacts, dynamic touchpoints.** Artifacts stable in Coaches Office; chat is the attention layer.
4. **Continuous presence via intermittent touches.** Multiple messages across the week, not one Sunday dump.
5. **All three artifacts share the same visual DNA** — dark navy `#0A1628`, amber `#F5A623`, Inter typography.

## Infra pressure-tests for Manny

- Push notification scheduling for Tuesday 8am / 3pm / Wednesday noon
- Persistent artifact storage per user per week (readable from Coaches Office tab)
- User action tracking — did the Tuesday waiver claim land? Needed for Wednesday's acknowledgment line
- Reasoning data layer — can Sal cite actual "29% target share" numbers, or is this a FantasyPros/stats integration we need first?

## Scope sequencing

If we ship one first: **Waiver Report**. Highest utility, clearest action, most testable with users.

## Companion docs

- `AC Vision & Gap Analysis.md` — strategic rationale, decision tree, five behavior pillars
- `AC — Oh That's Cool Moments.md` — nine candidate features scored by lift and signature
- `ac-mockups/TTM v.2.png`, `Waiver Wire v.2.png`, `Trading Block v.2.png` — reference wireframes
