# Project: Australian Financial Literacy Cartoon Series (working title TBD)

## What this is
A YouTube cartoon series using AI-generated animated videos of anthropomorphic animals to teach financial skills to kids, young adults and adults simultaneously, via layered writing (kids follow the story, young adults get product-level detail, adults get targets and strategy).

## Non-negotiable constraints
- **Australia-first.** Use Australian products and terms: superannuation, HECS-HELP, offset accounts, ASX, PayID/Osko/BPAY, Moneysmart, high-interest savers, Afterpay/Zip. Exclude US-only concepts: checking accounts, Venmo/Zelle, 401k/Roth/IRA, 529 plans, US credit score ranges.
- **Spelling:** Australian English (colour, organise, cheque only if ever needed).
- **Punctuation:** no em dashes in any written output. Use commas, periods, en dashes, or restructure.
- **Tone:** the lead never lectures or sounds smug. Story first, lesson embedded.
- **Compliance note:** general information only, never personal financial advice. No specific product recommendations (generic "high-interest savings account", never a named bank product). Keep this in every script.

## Episode format (locked)
- 5–7 minutes (scale to 8–10 later based on retention)
- One core concept per episode, max one supporting idea
- Structure: 10–15s cold open hook → setup → the hit (problem) → the lesson (explainer space) → the turn → payoff + tag/teaser
- Every episode ends with a 3-line end card: (1) one-sentence rule, (2) one action to do today, (3) one number to aim for
- Numbers shown on screen are deliberately ordinary ($640 repair, $40 rent rise) so adults recognise them

## Series brand devices
- The glowing gold pouch = savings. Characters who "get it" earn their own glow on a personal item.
- Bear & bull recurring cameos as market-mood running gag.
- Reusable "pay packet sliced up" animation for budgeting/super episodes.

## Current state
- Episode 1 "The Pouch" (pay yourself first / emergency fund): script complete (episodes/ep01/script.md), OpenArt prompt pack complete (episodes/ep01/openart-prompts.md)
- Episode 2 teased: "Maggie vs. the Credit Card"
- All four characters approved (assets/series/). Environment plates done (assets/ep01/environments/). Storyboard complete: 28 panels reviewed and passed (assets/ep01/storyboard/README.md). Next: video (Section 4 of the prompt pack) and voices.
- Production platform: OpenArt (see docs/workflow.md for model choices and pipeline)

## Key files
- docs/series-bible.md — full curriculum and character roster
- docs/workflow.md — OpenArt pipeline, model selections, prompting conventions
- episodes/ep01/ — script + generation prompts
- prompts/style-string.txt — the global style string, paste-identical everywhere
- assets/series/ — approved character designs (KANGA done); always attach these as references, never regenerate from text
- assets/ep01/ — generated reference art and the asset manifest

## When writing new episodes
1. Pick the next concept from the curriculum order in docs/series-bible.md
2. Cast from the roster (match animal theme to concept)
3. Follow the locked episode format above
4. Produce script.md first (26–30 shots, character bible header, production notes), then openart-prompts.md following the ep01 pattern: style string → characters → environments → storyboard list → Smart Shot sequences → image-to-video motion prompts → voice specs → assembly order → credit tips
