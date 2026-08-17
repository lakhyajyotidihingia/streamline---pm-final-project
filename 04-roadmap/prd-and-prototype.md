# Spotlight Curated Rail, Simplified PRD (StreamLine)

**Author:** Me · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** A film-literate, engaged long-time user who watches deliberately rather than passively

## 1. The Big Picture
- **Vision:** To increase length  of watch sessions of  film literate users by providing hand picked titles to watch and promoting a more direct engagemt
- **Press release:** Today, Streamline has provided its user a more personal touch for choice of available titles by understanding user preference better and more control on discoverability.
- **Success metric:** % Increase in sessions / wk with existing primary content mix
- **Guardrail:** content search then played ratio not less than 0.8

## 2. The Details
### User stories
- As a film literate user I want a list of handpicked titles available on my home page upon login So that I am able to start watching the titles without having to discover by searching for it
### Screens to build
- 1. Home Screen that displays top 10 hand picked titles
- 2. Separate screen to display details of the handpicked title clicked
- 3. Suggestions screen that matches that displays titles aligned in genre, popularity, cast and critics ratings
### Functional requirements
- The system must display 10 top titles hand picked to user in the Home Screen
- The system must provide a refresh button to refresh the displayed titles with new ones which matches user preference
- The system must display 5 suggestions apart from the handpicked titles that  align in genre, popularity, cast and critics ratings
### Smart behaviors (Situation → Outcome)
- If user clicks on a title to see its  details, details are displayed in a separate detail screen and similar titles are shown underneath
- If user refreshes the handpicked titles screen the suggested titles screen is not cleared automatically and displays the last shown titles. It refreshes only when user chose to see details of a new hand picked title.
### Technical constraints
- no APIs, no chat window

## 3. The Logistics
### Features out
- No history required
### Edge cases & safety guard
- No hand picked title clicked will not result in errors in other screens
### Decision log
- No search functionality to skew algorithm bias
- Suggested titles within same genre of selected hand-picked title for details
### Evals
- Detail screen displayed for selected title within 100ms
- Suggested titles displayed within 1 s
- Home Screen hand picked titles refreshed within 100 ms

## MoSCoW scope
- **Must:** Homepage rail placement — a distinct row on the homepage, positioned above or adjacent to "Because you watched," so it's seen in the same session as the misery moment.; Fully editorial title selection, zero algorithmic input — the rec engine (BUG-1091) has no write access to this rail's contents. This is the entire point of the feature; any algorithmic blending defeats it.; Admin/CMS mechanism for curators to add, order, and remove titles — engineers can't hand-code the rail in prod every week; editorial ops needs a basic interface to operate it without an engineer.; Static rail rendering on the existing homepage rail component — reuse the current rail UI (poster art, title, tap-to-detail) rather than building new front-end primitives from scratch. No time for novel UI this sprint.; Manual refresh capability — someone can update the rail's contents without a deploy. Doesn't need to be pretty; needs to exist.; Click → detail page → play instrumented — this rail must report into the search→played guardrail and sessions/wk metric, or we can't prove it worked.
- **Should:** "Hand-picked" or curator-attribution label on the rail — signals to the film-literate persona that this row is different in kind, not just position, from the algorithmic rails. Reinforces trust, but the rail works without it.; Basic scheduling (set a title live/expire date) — reduces ops burden of manual swaps, but a curator can do this by hand in week one.; Simple performance dashboard (CTR, plays) for the curation team — helps curators improve picks over time, but we can pull raw numbers manually for now.; Rail title cap / rotation logic (e.g. 8–12 titles, oldest rotates out) — prevents rail staleness, but a curator can manually manage a short list without code enforcing it.
- **Could:** Personalization overlay on top of the curated set (e.g. curators pick 20, lightweight logic picks which 8 show per user) — reintroduces algorithmic involvement, which is exactly what we're avoiding until BUG-1091 is actually fixed via A5.; Multiple themed rails (e.g. "Directors' Picks," "Deep Cuts") instead of one general rail — richer, but multiplies CMS and design surface area before we know one rail works.; Curator bios or "why we picked this" annotations per title — narrative depth for the film-literate persona, but a copy/design lift beyond sprint scope.; A/B testing framework for rail position or title count — useful once volume of data justifies it; premature with one rail and three weeks.
- **Won't (now):** Any machine-learning or algorithmic ranking within the rail. This is the feature's reason for existing. Reintroducing it here is the same failure as BUG-1091 in a new coat of paint.; User-following of individual curators. That's A7 (Curator Profiles) — a separate, larger feature we've already deferred to backlog.; Personalized/per-user rail variants. One editorial rail, same for all users, this sprint. Segmentation is a V2+ conversation.; Mobile-native custom layout distinct from the existing rail component. Ship on the current responsive rail; no bespoke mobile treatment this sprint.; Automated curator recommendations or AI-assisted picking tools. Curators pick manually. Tooling to help them pick faster is a later efficiency project, not a v1 requirement.; Localization of curated picks by region/language. Single global (or single-market) rail for v1; regional curation is a scaling problem for later.

---
**Builder hook:** Build a working prototype based on this PRD. Use the User Story as the core flow, Functional Requirements as build constraints, and prioritize speed and clarity over visual complexity.
