# Experimentation Plan (Module 5)

## Get your documents ready
- **From M3, your hypothesis sentence:** Based on Priya's reported dead-end search pattern (UXR-01) and the funnel data showing content-searched-then-played fell from 41% to 34%, I believe that solving pre-play discovery failure for Power User subscribers like Priya will result in deeper, more consistently rewarding sessions, as measured by a 5+ point recovery in content-searched-then-played rate (34% toward the 41% baseline) within 90 days. I will protect Power User sessions/week (currently 4.8×) so that narrowing the discovery surface doesn't suppress the browsing behavior that already defines this segment. I will make a go/no-go decision after one full 90-day cohort cycle, scaling on a ≥5 pt recovery, pivoting if flat, and killing if sessions/week declines.
- **From M3, your primary success metric & guardrail metric:** Content-searched-then-played rate for Power Users, recovering toward or above the 41% prior baseline (from current 34%). 
User sessions/week (currently 4.8×) must not decline - curation narrowing the discovery surface should not come at the cost of the browsing frequency that already defines this segment's engagement.
- **From M4, the feature you scoped in your PRD this is what you're testing:** Advanced Filter Engine, Filters by decade, language and runtime attack Priya's "can't find what I need" friction, which is the search-then-play recovery from 34% toward 41%.

## Define your experiment parameters
- **Feature under test pull from your M4 PRD:** Advanced Filter Engine (A9) -  filter by decade, language, and runtime, applied to the existing search/browse grid, per the M4 PRD.
- **Persona pull your M2 persona:** Priya, 34,  a 14-year, heavy-usage subscriber who has outgrown the platform's ability to serve her (UXR-01).
- **Expected outcome the behaviour change you expect, from your M3 hypothesis:** Giving Priya direct, explicit control to narrow the catalog herself — instead of relying on an algorithm that no longer reflects her taste - increases the rate at which her searches end in a play, without reducing how often she opens the app to browse.
- **Primary success metric the one number that defines success, from M3:** Content-searched-then-played rate for Power Users.
- **Baseline rate today's rate of your primary metric, from your M3 data:** 34% (today's rate - this is the number the experiment measures against, not the 41% historical target; 41% is the recovery goal, not the starting point for calculating lift).
- **Guardrail metric & boundary what must not break, and how far it can move before you investigate:** Power User sessions/week, currently 4.8×. 
Boundary: if the variant's session rate drops more than 2% relative to control (i.e., below ~4.7×) at any point during the test, halt and investigate before considering a ship - regardless of what the primary metric shows. This is a trap worth naming explicitly, since it's easy to let a primary metric win quietly erode the guardrail: a filter that increases search-then-play by making the catalog feel "solved" faster could also give her fewer reasons to keep coming back and browsing casually.
- **Minimum Detectable Effect (MDE) the smallest improvement worth shipping, your floor:** Minimum Detectable Effect (MDE) - 3 percentage points (34% → 37%). This is set as the floor because A9 is a Major Project (Effort 4) -  it's expensive enough that a marginal 1pp lift wouldn't justify permanent engineering investment, but 3pp is a meaningful fraction of the 7pp gap back to the 41% baseline and would still be a clear, ship-worthy signal.
- **Sample size per arm use the calculator in the builder, baseline + MDE:** Using baseline 34%, MDE 3pp (variant target 37%), 80% power, 5% significance (two-sided): ~3,990 Power Users per arm (≈8,000 total), by the standard two-proportion z-test calculation. Plug 34% and 3 into the builder's calculator to confirm the exact figure - this is a hand-calculated estimate, not the tool's output.
- **Traffic split & test duration 50/50 standard · cover ≥ 2 weekly cycles:** 50/50 split. Minimum 2 weekly cycles, but given Priya's cadence is a weekly session pattern (4.8×/week), I'd run 3 weeks rather than the 2-week floor - one extra cycle to smooth out a first-week novelty effect on a feature that's explicitly about habit (search-then-play), not just curiosity.
- **Significance threshold p < 0.05 is standard, explain any deviation:** p < 0.05, standard, two-sided. No deviation: this isn't a high-asymmetric-risk decision (e.g., safety, revenue-critical, irreversible), so there's no reason to tighten to p < 0.01 or loosen to a one-sided test.

## Define your control and variant
- **Control (A) the current experience, reference your M2 moment of misery and M3 funnel/workflow data:** The current search/browse experience with no filtering capability: Power Users land on the existing algorithmic rail and search results with no way to narrow by decade, language, or runtime. This is the arm where the moment of misery persists as-is — users can't easily find what they need, lose interest, and stop using the app — and it's the arm that produces the current 34% search-then-play baseline.
- **Variant (B) your single change, copy the relevant screens & functional requirements from your M4 PRD:** The current search/browse grid, unchanged, with the Advanced Filter Engine added on top, per the M4 PRD:

Entry point: the existing search/browse grid, with a visible "Filters" control added.
Feature core: the filter panel/drawer - decade, language, and runtime controls, a live result count, "Clear all," and "Apply."
Success/confirmation: the same browse grid, re-rendered with active filter chips above the results and the filtered title set in place.
Functional requirements in effect: filters combine with AND logic; active filters persist across in-session navigation; a single "Clear all" restores the full result set; each filter is individually removable as a chip; zero-result combinations show an empty state with "Clear all" as the recovery path.

This is the single change under test: everything else about how Priya reaches the search/browse grid stays identical between arms.
- **Isolation check, what has NOT changed? list everything identical between arms (app version, recommendation engine, notifications, onboarding). If something changed inadvertently, your test is compromised.:** The recommendation/curation algorithm powering the rail itself (unchanged in both arms - A9 filters on top of it, it doesn't replace it).
The underlying catalog and metadata (decade, language, runtime fields already exist; no new content or metadata pipeline introduced for the test).
Search functionality itself - how a query returns results before any filter is applied.
Onboarding, navigation structure, and app version/build otherwise.
Notifications, emails, and any other engagement surfaces (A6 Spotlight Digest Email, A2 "Why You'll Love This" Label, A1 Curated Rail  - none of these are live or altered in either arm).
Account, billing, and subscription experience.
Any other in-flight feature or experiment running concurrently on the same Power User segment - worth explicitly checking with the experimentation team before launch, since an overlapping test (e.g., a rail redesign) would confound attribution even if nothing on your side changed.

If any of these shifted between arms - say, a routine app release ships mid-test with an unrelated UI tweak to the grid - the result can no longer be attributed cleanly to the filter engine, and the test should be flagged or restarted.

## Formalize your hypothesis & shipping criteria
- **Your hypothesis (filled in):** I believe that the Advanced Filter Engine for Priya (a 14-year, heavy-usage subscriber who has outgrown the platform's ability to serve her) will result in her being able to narrow the catalog herself and go from search directly to play, instead of scrolling an algorithmic rail that no longer reflects her taste,
as measured by a 3 percentage point change in content-searched-then-played rate for Power Users within 3 weeks.
We will protect Power User sessions/week (currently 4.8×) throughout the test.
- **Your shipping criteria (filled in):** We will SHIP if content-searched-then-played rate improves by ≥ 3 percentage points at p < 0.05
and Power User sessions/week does not drop more than 2% relative to control (below ~4.7×) after 3 weeks.

We will ITERATE if direction is positive but lift is below 3 percentage points — investigate which filter type (decade, language, or runtime) is driving partial adoption before deciding whether to extend the test or rework the feature.

We will KILL if content-searched-then-played rate shows no improvement or moves negatively, or if Power User sessions/week breaches the guardrail boundary regardless of what the primary metric shows.

The read date is fixed at the end of 3 weeks. No results reviewed before this date.
- **Hardest parameter to define, and did it change your hypothesis? quick debrief:** The guardrail boundary was the hardest one to pin down. The brief only said sessions/week "must not decline," which isn't a testable rule — any single-digit noise in a 3-week window would technically be a decline. I had to convert that into a specific number (more than 2% relative drop, ~4.7×) before it could function as a real kill switch instead of a vague intention.

Defining it did sharpen the hypothesis, though it didn't change its direction: it forced the shipping criteria to be explicit that a strong primary-metric win does not override a guardrail breach. Without a hard boundary, it would be tempting to rationalize a small session dip as "worth it" if search-then-play jumped — which is exactly the failure mode the guardrail exists to prevent, since Priya's value to the business is partly her browsing frequency, not just her search precision.

