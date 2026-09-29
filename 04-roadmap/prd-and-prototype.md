# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** Advanced Filter Engine, Filters by decade, language and runtime attack Priya's "can't find what I need" friction, which is the search-then-play recovery from 34% toward 41%.
- **My finalized Must-Haves (after overriding the AI):**
1. Filter by decade (release year ranges) the single most-requested way a long-tenure user narrows a catalog she's mostly already seen once.
2. Filter by language/audio track, a distinct, non-overlapping cut that decade alone can't provide.
3. Filters combine (AND logic) and apply to the existing search results/browse grid, a filter that doesn't compose with search doesn't touch the search-then-play metric at all.
4. Persistent filter state across navigation within a session - if filters reset on every click, she re-filters every time, which risks the sessions guardrail by adding friction instead of removing it.
5. Clear/reset control, without it, a bad filter combination traps her in an empty result, recreating the exact misery this feature is meant to fix.
- **What I demoted from Must → Should/Won’t, and why:** The original Must Have said filters should persist "across navigation within a session" to avoid making her re-filter on every click. That held. But in the technical constraints pass, I explicitly ruled out cross-session and cross-device persistence, which the initial Must Have didn't yet distinguish from in-session persistence. This wasn't a full demotion to Should/Won't -  the core requirement (filters survive her moving around the grid) stayed a Must Have - but the broader version of "persistent" (surviving a closed tab, a new day, a different device) moved to Won't Have (Now).

Why: In-session persistence removes the friction that would hurt the guardrail (re-filtering on every click risks reducing her session frequency or patience). Cross-session persistence adds real value but requires a backend or account-level store, which is exactly the kind of scope creep the Must Have test was built to catch - "if removing it still lets the core persona succeed, it's not a must-have." She succeeds in this sprint if her filters hold while she browses; she doesn't need them to survive until tomorrow for the feature to solve today's moment of misery.

Everything else in the Must Have list held its ground through to the functional requirements without demotion - decade filter, language filter, AND-logic combination, and the clear/reset control all stayed Must Have because removing any one of them breaks the "narrow the catalog, then find something" loop that the whole feature exists to deliver.

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** The clearest one: filters combine with AND logic, not OR.

A vague brief - "let users filter by decade, language, and runtime" - would leave that ambiguous. An engineer could reasonably build OR logic (show me anything from the 90s, or in Spanish, or under 90 minutes), which produces a broad, noisy result set. That's a materially different feature, and it actively works against the reason A9 exists in the first place: Priya isn't trying to see more of the catalog, she's trying to cut it down to a small, precise set she can search-then-play from. OR logic would leave her scrolling again, which is the exact moment of misery this feature is supposed to end - and it does nothing for the 34%→41% recovery it's meant to drive.

Making the AND/OR decision explicit in the PRD closes off a branch that looks like a minor implementation detail but would have quietly shipped a feature that doesn't solve the problem it was built for.

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** Prototype exposed a real gap is the empty-state / zero-result path. The PRD says a bad filter combination should show "Clear all" rather than a blank grid, but it never specified what else, if anything, lives on that screen - is it only a button, or does it also suggest loosening one specific filter, or drop back to unfiltered results automatically? Until you actually build the screen, that ambiguity doesn't surface.
- **My prototype, as a link or a screenshot (publish or share from your tool; in Lovable that is Share → Share Preview, in Bolt Publish → Web. No share URL? Screenshot the working flow):** https://lovable.dev/projects/356b9207-61f6-4c57-b675-599cdd606953

