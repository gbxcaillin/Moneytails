# Project: Money Tails (Australian financial literacy cartoon series)

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
- All four characters approved (assets/series/). Environment plates done (assets/ep01/environments/). Storyboard complete: 28 panels reviewed and passed (assets/ep01/storyboard/README.md). Video: Seedance 2.5 in 30 s chunks; chunk 1 (shots 1 to 3) drafted at 480p, v2 passed with distinct voices and more movement (assets/ep01/video/). Kanga voice reference cut from the opener (assets/series/kanga/kanga-voice-ref-opener.mp3). Next: chunks 2 to 11 at 480p, then 1080p re-renders of approved chunks.
- Opener "The Coin Trail": DONE as a single 30 s Seedance 2.5 pass with audio with a soundtrack pass (assets/series/opener/seedance/opener-seedance25-v2-audio.mp4: theme, coin chimes, Kanga's intro lines, group cheer; prompts in seedance/, manifest in assets/series/opener/README.md). Ends on the five-tail title card and fades to black. Earlier pinned-shot rounds kept as fallback. Next: editor polish if needed, then Episode 1 video and voices.
- Production platform: OpenArt (see docs/workflow.md for model choices and pipeline)

## Key files
- docs/series-bible.md — full curriculum and character roster
- docs/opening-sequence.md — title sequence, theme music, typography and colour brief. Locked: Coin Trail opener, five-tail logo. Music, fonts, vocal still proposals.
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
