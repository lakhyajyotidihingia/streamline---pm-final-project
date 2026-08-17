# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** Spotlight Curated Rail: Hand-picked homepage rail that bypasses the algorithm
- **My finalized Must-Haves (after overriding the AI):** Homepage rail placement — a distinct row on the homepage, positioned above or adjacent to "Because you watched," so it's seen in the same session as the misery moment.
Fully editorial title selection, zero algorithmic input — the rec engine (BUG-1091) has no write access to this rail's contents. This is the entire point of the feature; any algorithmic blending defeats it.
Admin/CMS mechanism for curators to add, order, and remove titles — engineers can't hand-code the rail in prod every week; editorial ops needs a basic interface to operate it without an engineer.
Static rail rendering on the existing homepage rail component — reuse the current rail UI (poster art, title, tap-to-detail) rather than building new front-end primitives from scratch. No time for novel UI this sprint.
Manual refresh capability — someone can update the rail's contents without a deploy. Doesn't need to be pretty; needs to exist.
Click → detail page → play instrumented — this rail must report into the search→played guardrail and sessions/wk metric, or we can't prove it worked.
- **What I demoted from Must → Should/Won’t, and why:** None

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** None

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** None
- **My shareable prototype URL (Lovable: Share → Share Preview · Bolt: Publish → Web):** https://lovable.dev/preview/M7aT450KDyjpfrATrBU1cPKdh6jlDBFP
