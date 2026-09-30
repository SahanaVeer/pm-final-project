# GTM Launch Plan, StreamLine (B2C)

| Field | Value |
|---|---|
| Feature | Advanced Filter Engine |
| Goal | Engagement |
| Launch tier | L, Multi-channel |

## Goal & Audience
- **Goal:** Engagement, Advanced Filter Engine isn't a new-user acquisition feature and it isn't built to move a revenue metric directly - it's built to solve a specific, already-diagnosed friction for an existing, high-value segment. Priya and Power Users like her already use StreamLine 4.8×/week; the problem isn't that they don't know the product exists (Awareness) or that they need a reason to pay (Conversion). The problem is that a 14-year relationship with the catalog has outgrown what the algorithm can serve them, and search-then-play has degraded from 41% to 34% as a result.

That's a textbook engagement problem: the goal isn't to bring new people in, it's to get an already-engaged segment to use a specific new capability deeply enough that it changes their core behavior (search ending in play) without disturbing the behavior that already defines them (session frequency). The A/B brief's primary metric (search-then-play rate) and guardrail (sessions/week) are both engagement metrics, not awareness or conversion metrics - so Engagement is the goal that's already implicit in the M3 hypothesis and M5 experiment design. Naming it explicitly now just makes sure the audience, channels, and enablement plan in the next steps stay aimed at existing Power Users, not at top-of-funnel reach.
- **Target audience:** Heavy-usage subscriber who has outgrown the platform's ability to serve

## Launch Tier
- **L, Multi-channel**, Reach: This is a narrow segment by design — Power Users, not the full subscriber base. A feature aimed at people like Priya doesn't need company-wide comms, press, or an event; it needs to reach a specific, identifiable slice of long-tenure heavy users who are actually experiencing the moment of misery this feature solves.

Revenue impact: The feature isn't directly monetization-facing - it's an engagement play protecting a segment that's already valuable (4.8× weekly sessions) from quietly eroding. That's real but indirect revenue risk (retention of high-LTV subscribers), not a new revenue stream to headline with a big launch. It doesn't justify XL-scale investment, but it's meaningful enough that it can't be shipped silently either.

What silence would risk: This is the deciding factor against going smaller (S). If Advanced Filter Engine ships with zero outreach, the exact users it's meant to help - long-tenure Power Users who've likely stopped expecting the product to change for them — may never discover the "Filters" control sitting on a screen they've stopped exploring closely. A feature built specifically to reverse a metric decline for a segment that's disengaging can't rely on organic discovery; silence here means the fix exists but doesn't reach the people it was built for, and the 34%→41% recovery never materializes because they never find the entry point.

That combination - narrow reach, indirect but real revenue stakes, and a real cost to silence - points to M, not S (too quiet for a fix this targeted) and not L/XL (multi-channel or full press/events would be over-investment for a segment this specific and a feature that isn't acquisition-facing).

## Channels
1. **Owned: In-app contextual prompt/tooltip on the search & browse grid -  This is the highest-leverage channel for this launch: Priya is already in the exact surface where the feature lives, 4.8× a week. A one-time contextual highlight on the new "Filters" control (e.g., a subtle badge or a dismissible tooltip the first time a Power User lands on the grid post-launch) meets her at the moment of misery itself, rather than asking her to learn about the feature somewhere else and remember to look for it later.**
2. **Owned: Targeted email to the Power User segment - A single, short email to subscribers matching the Power User definition (session frequency, tenure), framed around the specific friction ("finally, filter by decade, language, or runtime") rather than a generic feature announcement. This directly addresses the "risk of silence" from Step 2 - it's the channel that reaches her even if she doesn't happen to notice the in-app prompt that week, and email is naturally scoped to exactly the narrow segment this launch targets.**
3. **Owned: In-app "What's New" / release notes surface -  A secondary, lower-friction touchpoint for Power Users who check release notes as part of their regular habit (common in long-tenure, heavy-usage users who've watched the product evolve for years). It also gives the feature a discoverable, permanent record independent of the timing of the tooltip or email.  All three are Owned - appropriate for an M-sized, engagement-focused, non-monetization launch aimed at a narrow existing segment. Earned (press/media) and Paid (ads) would be over-investment here: this isn't a feature that needs external validation or new-user acquisition spend, and reaching for either would work against the "targeted, focused comms" sizing decided in Step 2.**

## Enablement & Assets
Support/CS FAQ: A short internal doc covering what the filters do, how AND-logic combination works (e.g., "decade + language" narrows, doesn't broaden), what happens on a zero-result combination (empty state + Clear all), and that filter state resets each session (not persisted) — this last point is the most likely source of confused tickets ("my filters disappeared").
In-app tooltip copy + design asset: Short, one-line copy for the contextual prompt, built to the same visual system as the filter panel itself (already established in the M4/M5 prototype).
Email copy + template: One short email, no press-release-scale copy needed — plain, direct, framed around the friction ("find something new after 14 years"), not a general feature list.
Release notes entry: A 2-3 sentence description for the What's New surface, consistent in tone with the email.
No Sales enablement needed: this isn't a sales-assisted or upsell-driving feature, so there's no deck, pitch, or talk track required - worth noting explicitly so Sales doesn't get looped in on a launch that isn't theirs to carry, consistent with A8/A10 being Sales-originated requests you already cut from this initiative on persona-fit grounds.

## Ownership, Budget & Timeline
- **Ownership & budget:** Feature build (filter panel, AND logic, chips, empty state) - Owner: Engineering Lead (2 eng, per M4 constraints). No extra cost - already scoped in sprint capacity.
QA on edge cases (zero-result, chip removal, session persistence) - Owner: Engineering Lead. No extra cost; must complete before Phase 2.
In-app tooltip design + copy - Owner: Designer (1 designer, per M4 constraints). No extra cost if built alongside the core feature UI, but flag the risk: designer capacity may be fully consumed by the feature build itself, leaving a gap for this asset.
Power User segment definition + email list pull - Owner: PM, with Data/Analytics. No extra cost; dependent on segment/session data being queryable ahead of launch.
Targeted email copy + send - Owner: PM, sent via CS/Lifecycle marketing tooling. Minor cost only if the email platform has per-send fees; otherwise owned infrastructure.
Release notes entry - Owner: PM. No cost.
Support/CS FAQ doc - Owner: PM, reviewed by CS Lead. No cost, but book CS Lead review time in advance rather than assuming availability.
Experiment monitoring (primary metric + guardrail) — Owner: PM, with Data/Analytics. No extra cost; this is the one activity with a hard deadline (3-week read date) — missing the monitoring cadence risks reading results late or reacting to noise.

Asset gap to flag explicitly: the tooltip and in-app prompt depend on designer time that's also fully committed to the feature build (1 designer total, per constraints). If design capacity is tight, treat the tooltip as a Should Have for launch, not a Must Have — decide this now rather than discovering it mid-Phase 2.
- **Timeline:** Phase 1 — Beta (Weeks 1–3, concurrent with the A/B test)

Feature ships to the 50/50 experiment split only - not a full rollout yet.
No external comms in this phase: the email, tooltip, and release notes are held until the experiment reads out, since promoting a feature that might still be killed would create a rollback/comms problem.
Owner: Engineering Lead ships to experiment population; PM monitors primary metric and guardrail daily against the fixed 3-week read date.

Phase 2 - Launch moment (Week 4, immediately following the read date)

Triggered only by a SHIP decision from the shipping criteria - this phase doesn't start on a calendar date independent of the experiment result.
Full rollout to all Power Users.
In-app tooltip goes live day one; targeted email sends same week; release notes entry publishes same day as rollout.
Owner: PM coordinates the send sequence; Engineering Lead handles rollout; Designer's tooltip asset goes live with the rollout, not before.

Phase 3 - Post-launch (Weeks 5–8)

Monitor adoption of the filter feature itself (usage rate, which filter types are used) beyond the original experiment window, since the A/B test measured search-then-play lift but not which filter dimension drove it - this is where that gap gets closed.
CS/Support monitor ticket volume against the FAQ to catch confusion points (e.g., non-persistent filter state) the experiment population may not have surfaced at scale.
Owner: PM leads the post-launch review; Data/Analytics provides the adoption breakdown; CS Lead reports ticket trends.
Decision point at end of Phase 3: whether Should Have items (runtime filter refinements, result count preview, saved presets) move into a future sprint, based on real usage data rather than the original PRD assumptions alone.

## Success Metrics
- **Metrics:** Content-searched-then-played rate for Power Users — the primary metric from the A/B brief, target 34%→37%+ within the 3-week experiment window. This is the direct measure of whether Priya's "can't find what I need" friction is actually resolving, and it stays the anchor metric through launch, not just the test.
Filter feature adoption rate - % of Power User sessions that engage the filter panel at all, tracked into Phase 3. This wasn't part of the A/B primary metric but is essential post-launch: without it, you can't tell whether a search-then-play lift came from broad adoption or a small subset of heavy filterers, which is exactly the attribution gap the isolation pressure-test flagged earlier.
Power User sessions/week (guardrail, held through launch) — still 4.8×, still protected. An Engagement launch that improves the primary metric while quietly eroding this one hasn't actually succeeded - it's just moved the problem.

Deliberately excluded: any conversion or revenue metric (e.g., upgrade rate, retention-driven LTV). Given the Engagement goal set in Step 1, measuring this launch by a revenue number would be the exact misread the prompt warns against — reading an engagement fix through a conversion lens would either falsely credit it for revenue movement it didn't drive, or falsely kill a working feature because it didn't move a number it was never built to move.
- **Bad signal to watch for:** A rise in search-then-play rate accompanied by a flat or declining filter adoption rate. That combination would mean the lift isn't actually coming from the feature you shipped — it's either noise, a concurrent confound (something else changed in the same window), or a seasonal/content-calendar effect unrelated to filtering at all. A win on the headline metric with no adoption to explain it is a signal to investigate before celebrating, not a green light.
- **Likely post-launch decision:** Iterate, not stop or scale as-is. Given that the variant bundles three filter dimensions into one launch (flagged in the isolation pressure-test), the most probable outcome is a real but partial win: search-then-play improves, but adoption data in Phase 3 reveals that one filter type (most likely language or decade, given how directly they map to a 14-year user's "already seen this" problem) is doing most of the work while runtime sees light use. That would trigger a scoped iteration — refining or simplifying the underused filter, or investing further in the one driving results — rather than a binary ship-and-done or kill decision.
