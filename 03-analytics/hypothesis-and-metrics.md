# Hypothesis & Success Metrics (Module 3)

## Pre-work · Hypothesis check
- **Role , who you are solving for (from M2):** A film-literate, engaged long-time user who watches deliberately rather than passively.
- **Goal , what this user is ultimately trying to achieve:** Find titles that reflect their actual, nuanced taste — not just their most recent click.
- **Friction / moment of misery , the specific pain blocking their goal:** After watching a single action film, the "Because you watched" row recommended three more near-duplicate action sequels — prompting the reaction "I'm not a genre, I'm a person." This is corroborated by BUG-1091 (High severity): the recommendation engine surfaces same-franchise, low-diversity titles rather than genuinely tailored ones. The moment of misery is being reduced to a single data point by a system that mistakes repetition for personalisation.
- **Current workaround , the external tool or manual process they rely on (M2):** The user replaced the product with a competitor's curation service, and then cancelled the subscription entirely
- **Problem Hook , your one-sentence framing of the business crisis (M1):** We must solve matching of available titles curated to user's likes and dislikes and make discoverability frictionless
- **Value Proposition , the outcome your initiative promised to deliver (M1):** For our users, we will deliver better discoverability of our titles so that do not lose our users to competitors who provide better experience by understanding their preference

## Read your data snapshots
- **Does the funnel data confirm your M2 friction point, or does it tell a different story? Note where the numbers align with the qualitative pain you found and where they diverge.:** The funnel tells me a somewhat different  story. M2 friction tells me about issue of personalisation. The quantitative data tells me about engagement in the title played. It does indicate me that the user could be leaving the session sooner due to lack of interest in the content which again indicates not being catered preferred content to the user.
- **Do the retention patterns align with the workaround your M2 persona used to find content? Note what the Mo. 0→1 drop suggests about the onboarding experience your persona described as frustrating.:** M0->M1 data suggest introducing Spotlight somewhat increased retention due to suggestion provided beforehand rather than exploring full catalog. Thus increasing discoverability for the user by highlighting content that the user might not have discovered.
- **Does the LTV gap and the content mix (61% trending for Wanderers) confirm the moment of misery your persona described? Note which segment your persona is in and whether the data confirms their pain.:** Yes, it confirms the moment of misery. My persona seems to be in Wanderers.
- **Does the low adoption confirm your persona is burdened by tools they don’t use? Note whether the low scheduling adoption (42%) for coordinators matches your M2 moment of misery.:** _(not filled in)_
- **Does the workflow data match the manual process or hack you documented in M2? Note whether the specific drop-offs or time gaps explain why your persona avoids the digital tool.:** _(not filled in)_
- **Look at the CSAT heatmap. Which specific cell most directly maps to your persona’s friction? Note how the NPS trend justifies the urgency of your M1 Problem Hook.:** _(not filled in)_

## Step 3 · Craft your hypothesis
- **Qualitative evidence (from M2) , quote the specific friction / moment of misery for your persona:** After watching a single action film, the "Because you watched" row recommended three more near-duplicate action sequels — prompting the reaction "I'm not a genre, I'm a person." Seems the personalisation and discovery of contents are  not efficient.
- **Quantitative evidence (from M3) , name the metric or data point that confirms the pain; cite the number:** % of users who are wandering and not exposed to discoverable contents
- **Persona , role, goal, and the friction you confirmed in the reconciliation steps:** A film-literate, engaged long-time user who watches deliberately rather than passively.
- **Problem you are solving , one sentence describing the specific friction this initiative removes:** Increase discoverability of relevant contents
- **Strategic outcome , what behaviour change do you expect, and how does it map to retention / revenue / churn?:** Users are able to discover wider and curated availability of contents leading to more engagements
- **Primary success metric (initiative signal) , the leading indicator that tells you the gap is closing:** Increased sessions / wk with existing primary content mix
- **Guardrail metric (product signal) , the metric that must NOT drop; it protects your existing base:** content search then played
- **Decision window , how much time or data before you scale, pivot, or kill? minimum threshold to proceed?:** 1 quarter
- **Draft your full hypothesis sentence , one to three sentences; quote the metric, name the persona, name the outcome:** Based on issue with personalised recommendation & % of user who are wandering, I believe that increase discoverability of relevant contents for film-literates ,will result in Users able to discover wider and curated availability of contents leading to more engagements, as measured by a 10% change in Increased sessions / wk with existing primary content mix. I will protect content search then played and will make a go/no-go decision after 1 quarter
