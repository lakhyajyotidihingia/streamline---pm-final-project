# Experimentation Plan (Module 5)

## Get your documents ready
- **From M3, your hypothesis sentence:** Based on issue with personalised recommendation & % of user who are wandering, I believe that increase discoverability of relevant contents for film-literates ,will result in Users able to discover wider and curated availability of contents leading to more engagements, as measured by a 10% change in Increased sessions / wk with existing primary content mix. I will protect content search then played and will make a go/no-go decision after 1 quarter
- **From M3, your primary success metric & guardrail metric:** primary success metric: Increased sessions / wk with existing primary content mix

guardrail metric:  content search then played
- **From M4, the feature you scoped in your PRD this is what you're testing:** Spotlight Curated Rail: Hand-picked homepage rail that bypasses the algorithm

## Define your experiment parameters
- **Feature under test pull from your M4 PRD:** Spotlight Curated Rail: Hand-picked homepage rail that bypasses the algorithm
- **Persona pull your M2 persona:** A film-literate, engaged long-time user who watches deliberately rather than passively
- **Expected outcome the behaviour change you expect, from your M3 hypothesis:** increase discoverability of relevant contents for film-literates ,will result in Users able to discover wider and curated availability of contents leading to more engagements,
- **Primary success metric the one number that defines success, from M3:** Increased sessions / wk with existing primary content mix
- **Baseline rate today's rate of your primary metric, from your M3 data:** 11% of visitors reach a 30+ minute session
- **Guardrail metric & boundary what must not break, and how far it can move before you investigate:** content search then played, +/- 5%
- **Minimum Detectable Effect (MDE) the smallest improvement worth shipping, your floor:** 5%
- **Sample size per arm use the calculator in the builder, baseline + MDE:** 733
- **Traffic split & test duration 50/50 standard · cover ≥ 2 weekly cycles:** 50/50
- **Significance threshold p < 0.05 is standard, explain any deviation:** p < 0.05

## Define your control and variant
- **Control (A) the current experience, reference your M2 moment of misery and M3 funnel/workflow data:** Users are unable to find consistency in listing or progress across devices
- **Variant (B) your single change, copy the relevant screens & functional requirements from your M4 PRD:** 1. Home Screen that displays top 10 hand picked titles
2. Separate screen to display details of the handpicked title clicked 
3. Suggestions screen that matches that displays titles aligned in genre, popularity, cast and critics ratings

The system must display 10 top titles hand picked to user in the Home Screen
The system must provide a refresh button to refresh the displayed titles with new ones which matches user preference
The system must display 5 suggestions apart from the handpicked titles that  align in genre, popularity, cast and critics ratings
- **Isolation check, what has NOT changed? list everything identical between arms (app version, recommendation engine, notifications, onboarding). If something changed inadvertently, your test is compromised.:** Same list of titles available

## Formalize your hypothesis & shipping criteria
- **Your hypothesis (filled in):** I believe that Spotlight Curated Rail for [ A film-literate, engaged long-time user who watches deliberately rather than passively will result in Users able to discover wider and curated availability of contents leading to more engagements,
as measured by a 5% change in Increased sessions / wk with existing primary content mix within 14 days
We will protect content search then played throughout the test.
- **Your shipping criteria (filled in):** We will SHIP if Increased sessions / wk with existing primary content mix  improves by ≥ 5% at p < 0.05
and [ontent search then played does not reach -5% after 14 days.

We will ITERATE if direction is positive but lift is below the MDE.

We will KILL if the primary metric shows no improvement or moves negatively.

The read date is fixed at the end of 14 days, no results reviewed before this date.
- **Hardest parameter to define, and did it change your hypothesis? quick debrief:** None
