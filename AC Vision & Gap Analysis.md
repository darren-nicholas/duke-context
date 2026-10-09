# Assistant Coach — Vision & Gap Analysis (Oct 2026)

**Purpose:** The strategic north star for AC — what it should BE vs. what it currently IS. Doubles as a Codex prompt for architectural thinking on how to close the gap. Lives in the vault for durable reference; mirrored to `duke-context` for Codex access.

Last updated: 2026-10-09
Author: Darren (with Claude Code as drafting partner)

---

## Who AC is for

Fantasy football players who want to make better decisions. Not stat nerds who already know everything. Not casual players who just want a "pick 1" answer. People in the middle who want to learn WHY while they play — and who want to feel like they have a coach, not a chatbot.

## The brand positioning

**"Powered by Actual Intelligence"** — explicitly anti-chatbot. Our coaches should feel like trusted human advisors who happen to have perfect data recall, not like a chatbot wearing a persona hat. **"Don't Get Bitter. Get Better."** — the mindset we're coaching toward.

---

## The vision — what AC should DO and FEEL

### Five behavior pillars

**1. Proactive, not reactive.**
Current AC waits for the user to ask. The vision: AC watches the user's roster, their league context, and the NFL news cycle, and SURFACES decisions and recommendations unprompted. It should feel like a coach who texts at 10am Tuesday: *"Hey — Flowers is a buy-low this week. Here's why."*

**2. Philosophy-driven, not projection-driven.**
Three coaches — Ray, Sal, Dee — each with a distinct philosophy. When a user hires Ray, EVERY decision AC makes should run through Ray's philosophy. If Ray prioritizes volume over efficiency, Ray's "start Flowers vs Addison?" answer should be *different* from Dee's — not just in tone, but in actual recommendation. Current state has personas with distinct voices; vision has personas with distinct DECISION RULES.

**3. Deep reasoning transparency.**
Every recommendation shows its work. Not *"start Flowers"* but *"start Flowers because: (1) 29% target share through 5 weeks, (2) opponent allows 180 YPG to WRs ranked by DVOA, (3) his historical pattern vs this scheme shows 1.2x his season average."* Users should get smarter at fantasy BY USING AC. **Reasoning transparency is our product moat** — competitors don't show it; we lead with it.

**4. Persistent context.**
AC should know the user's team, their league scoring (half-PPR vs standard vs full-PPR vs superflex), their record, their recent trades, their draft history, their waiver priority. Context should be deep and persistent, not re-queried every session.

**5. Trusted coach feel, not AI assistant feel.**
Language, cadence, and interaction patterns should feel like a human coach texting you — not an AI with pleasantries. *"Nick, start Flowers"* not *"Great question! Based on the data I have, I would recommend starting Flowers because…"* No "packet responses." No refusing to speculate on NFL teams. Opinionated. Direct. Specific. Occasionally pushes back on bad user decisions.

---

## The decision tree each coach should run

For every decision (start/sit, waiver pickup, trade evaluation, draft pick), the coach runs through this logic — but WEIGHTED differently per coach's philosophy:

- **User context** → user's record, playoff positioning, contending vs rebuilding, stated philosophy at onboarding
- **Roster context** → their current team, position needs, alternatives at each slot
- **Player signals**
  - Volume: target share, snap count, red zone touches, carries inside the 10
  - Efficiency: YPC, YAC, catch rate, true completion percentage
  - Trajectory: trending up/down over last 3 weeks
  - Health: injury status, workload concerns
- **Opponent signals**
  - DVOA by position allowed
  - Scheme matchup (zone vs man, blitz rate vs line protection)
  - Recent trends vs similar player types
  - Weather, Vegas totals, home/away splits
- **Market signals**
  - ADP vs current ranking
  - Trade market consensus
  - Waiver percentage ownership
  - Dynasty value (if applicable)
- **Philosophy filter**
  - Ray weights volume + trajectory heavily, discounts efficiency outliers
  - Sal weights opportunity + matchup, trusts advanced stats
  - Dee weights contrarian/value signals, hunts breakout opportunities
- **Output**
  - A specific recommendation
  - 2-3 cited reasons showing the signals weighted
  - Confidence level stated honestly (not "high confidence" by default)
  - A follow-up action the user should take

---

## Current state (what's shipped)

- iOS app on TestFlight, actively iterated (v39+)
- 3 coaches with Coach Prompt Specs plugged verbatim into system prompts
- LLM: Gemini 3.6-flash with per-request context injection
- Facts-from-context guardrail prevents hallucination of current NFL info
- "Ask Coach" is primarily reactive chat
- Monetization: FantasyPros API ($3K/year) is current data source, VIP pricing TBD
- Website: assistantcoachff.com with "Powered by Actual Intelligence" + "Don't Get Bitter. Get Better."
- One coach per user — hire at onboarding, no in-app switching in v1

## The gap I'm feeling

Current state: **"a chatbot with three personas on top of Gemini + context injection."**

Vision: **"a proactive philosophy-driven coach that watches your team, surfaces decisions with transparent reasoning, and feels like a trusted human advisor."**

Specific gaps:

1. **Proactivity gap** — AC doesn't watch the user's team or push notifications. It waits.
2. **Decision-divergence gap** — Not confident the three coaches actually give DIFFERENT recommendations yet. They may have different voices on the same underlying answer. Needs audit.
3. **Reasoning transparency gap** — Coaches may give opinions but the signal-weighting layer isn't surfaced in the UX. Users don't learn fantasy from AC; they get answers.
4. **Persistent context gap** — Context injection happens per-request; vision needs persistent user profile with league, roster, record, history.
5. **Feel gap** — Current voice might still feel too "AI assistant polite" and not enough "coach direct."

---

## What I need back (if this is a Codex prompt)

NOT code. Not yet. I need architectural / strategic thinking:

1. **For each of the 5 gaps above**, propose 2-3 approaches to close it. Flag which are prompt-engineering level (low lift) vs. backend infrastructure level (high lift).

2. **Identify the hardest gap** and explain why. Where will engineering effort concentrate?

3. **Propose a sequencing** — if I could only tackle 2 of the 5 gaps in the next 6 weeks before fantasy playoffs (Week 15 = early December), which 2 would move the needle most and why?

4. **Flag architectural dependencies** — if I build persistent context, does that unblock proactive notifications? If I nail decision-divergence first, does that unblock reasoning transparency? Where are the leverage points?

5. **Propose how to communicate this to Manny** — not a pitch deck, but a shape of document / scope that will land well with a technical co-founder who ships fast and doesn't want fluff.

## Constraints

- Manny is primary developer; I write specs, design, product. I do not push code to the AC repo.
- 2-person team, not VC-backed. Prefer solutions that don't require major infra investment.
- Gemini 3.6-flash is current LLM. Can switch if justified.
- No backend database currently; context is injected per-request. Can add if required.
- Fantasy playoffs start Week 15 (early December). Any big change should ship before then or wait until offseason.
- User base currently TestFlight beta. Can afford some risk in design decisions.

## Deliverable format

One-page markdown response. Be opinionated. Where I'm wrong about the vision, say so. Where I'm overcomplicating or undercomplicating, say so. I want your judgment, not just your writing. Don't fabricate specifics about my codebase; treat current state as described above.
