# Feature Roadmap, Module 4 · StreamLine Spotlight

**Team:** 2 engineers + 1 designer

## Strategic anchors
- **Persona:** A 14 -year, heavy-usage subscriber who has outgrown the platform's ability to serve her (UXR-01, Priya, 34).
- **Primary metric:** Content-searched-then-played rate for Power Users, recovering toward or above the 41% prior baseline (from current 34%).
- **Moment of misery:** Users can’t easily find what they need, lose interest, and stop using the app.
- **Guardrail:** Power User sessions/week (currently 4.8×) must not decline - curation narrowing the discovery surface should not come at the cost of the browsing frequency that already defines this segment's engagement.

## Scoring
| Feature | Value | Effort | Quadrant | Decision | Rationale |
|---|---|---|---|---|---|
| A1 Spotlight Curated Rail | 3 | 1 | Fill-In | Next | It bypasses the algorithm she has outgrown and ships in days, but it drives play without search, so it barely moves the primary metric. But alongside A9, It's a cheap test of curation. |
| A2 'Why You'll Love This' Label | 2 | 3 | Time Sinker | Later | Her problem is finding candidates, not choosing between them, and hover doesn't work on mobile. |
| A3 Hidden Gem Badge | 3 | 2 | Fill-In | Next | It gives a 14-year user a reason to explore titles she hasn't seen, but it's a label and doesn't help her find anything. |
| A4 Mood-Based Entry Point | 2 | 4 | Time Sinker | Cut | A login gate adds friction to every one of her 4.8 weekly sessions, which puts the guardrail at risk, and it needs a mood taxonomy across the catalog. |
| A5 Personalized Spotlight Queue | 3 | 5 | Time Sinker | Cut | It's more algorithmic personalization, which is what already failed her, and it's a heavy ML build with filter-bubble risk against the guardrail. |
| A6 Spotlight Digest Email | 1 | 2 | Fill-In | Later | She's already a heavy user, and an email does nothing for in-app search-then-play. |
| A7 Curator Profiles | 3 | 4 | Time Sinker | Cut | Human taste suits someone who has outgrown the algorithm, but the follow graph, profile pages and curator supply are too much for 2 engineers in 3 weeks. |
| A8 Watch Party (Spotlight) | 1 | 5 | Time Sinker | Cut | Synchronized playback and chat are a multi-month Sales-driven build that never touches finding content. |
| A9 Advanced Filter Engine | 5 | 3 | Major Project | Now | Filters by decade, language and runtime attack Priya's "can't find what I need" friction, which is the search-then-play recovery from 34% toward 41%. They add discovery paths rather than narrowing them, so the 4.8× sessions guardrail is safe. |
| A10 Offline Download (Spotlight) | 1 | 5 | Time Sinker | Cut | Rights, DRM and storage make it a huge build, and it does nothing for the primary metric. |

## Roadmap
### NOW, 3-week sprint
- **A9 Advanced Filter Engine**, Filters by decade, language and runtime attack Priya's "can't find what I need" friction, which is the search-then-play recovery from 34% toward 41%. They add discovery paths rather than narrowing them, so the 4.8× sessions guardrail is safe.

### NEXT, following 1-2 sprints
- **A1 Spotlight Curated Rail**, It bypasses the algorithm she has outgrown and ships in days, but it drives play without search, so it barely moves the primary metric. But alongside A9, It's a cheap test of curation.
- **A3 Hidden Gem Badge**, It gives a 14-year user a reason to explore titles she hasn't seen, but it's a label and doesn't help her find anything.

### LATER, backlog
- **A2 'Why You'll Love This' Label**, Her problem is finding candidates, not choosing between them, and hover doesn't work on mobile.
- **A6 Spotlight Digest Email**, She's already a heavy user, and an email does nothing for in-app search-then-play.

### ✂ Cut List
- **A4 Mood-Based Entry Point**, A login gate adds friction to every one of her 4.8 weekly sessions, which puts the guardrail at risk, and it needs a mood taxonomy across the catalog.
- **A5 Personalized Spotlight Queue**, It's more algorithmic personalization, which is what already failed her, and it's a heavy ML build with filter-bubble risk against the guardrail.
- **A7 Curator Profiles**, Human taste suits someone who has outgrown the algorithm, but the follow graph, profile pages and curator supply are too much for 2 engineers in 3 weeks.
- **A8 Watch Party (Spotlight)**, Synchronized playback and chat are a multi-month Sales-driven build that never touches finding content.
- **A10 Offline Download (Spotlight)**, Rights, DRM and storage make it a huge build, and it does nothing for the primary metric.

[streamline-spotlight-roadmap.html](https://github.com/user-attachments/files/32659769/streamline-spotlight-roadmap.html)

