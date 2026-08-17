# A/B Experiment Brief, StreamLine (B2C)

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | Spotlight Curated Rail |
| Persona | A film-literate, engaged long-time user who watches deliberately rather than passively |
| Expected outcome | increase discoverability of relevant contents for film-literates ,will result in Users able to discover wider and curated availability of contents leading to more engagements, |
| Primary success metric | Increased sessions / wk with existing primary content mix |
| Baseline rate | Current 11% of visitors reach a 30+ minute session |
| Guardrail metric | content search then played |
| Guardrail boundary | retention must not drop 5% |
| Second guardrail | · |
| Minimum Detectable Effect | +5 pts |
| Sample size per arm | 1000 |
| Traffic split | 50/50 |
| Test duration | 14 days |
| Significance threshold | p < 0.05 |

## Control vs. Variant
- **Control (A):** Users are unable to find consistency in listing or progress across devices
- **Variant (B):** 1. Home Screen that displays top 10 hand picked titles
2. Separate screen to display details of the handpicked title clicked 
3. Suggestions screen that matches that displays titles aligned in genre, popularity, cast and critics ratings

The system must display 10 top titles hand picked to user in the Home Screen
The system must provide a refresh button to refresh the displayed titles with new ones which matches user preference
The system must display 5 suggestions apart from the handpicked titles that  align in genre, popularity, cast and critics ratings
- **Held constant (isolation check):** Same list of titles available

## Hypothesis
> I believe that Spotlight Curated Rail for A film-literate, engaged long-time user who watches deliberately rather than passively will result in increase discoverability of relevant contents for film-literates ,will result in Users able to discover wider and curated availability of contents leading to more engagements,, as measured by a +5 pts change in Increased sessions / wk with existing primary content mix within 14 days. We will protect content search then played throughout the test.

## Shipping criteria
> We will **ship** if Increased sessions / wk with existing primary content mix improves by ≥ +5 pts at p < 0.05 and content search then played does not reach retention must not drop 5% after 14 days.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 14 days, no results reviewed before this date.
