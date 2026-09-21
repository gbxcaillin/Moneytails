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
- Screen time rule: the idea gets the frame. Character-only beats run 2 to 4 seconds; about two thirds of the runtime shows the concept itself (money moving, the pouch, the pay packet, balances, the explainer space). Gags are welcome with no quota, but each must either develop a character's idiosyncrasy or be about the episode's theme; never filler. Full rule in docs/series-bible.md.

## Series brand devices
- The glowing gold pouch = savings. Characters who "get it" earn their own glow on a personal item.
- Bear & bull recurring cameos as market-mood running gag.
- Reusable "pay packet sliced up" animation for budgeting/super episodes.

## Current state
- Episode 1 "The Pouch" (pay yourself first / emergency fund): script complete (episodes/ep01/script.md), OpenArt prompt pack complete (episodes/ep01/openart-prompts.md)
- Episode 2 teased: "Maggie vs. the Credit Card"
- All four characters approved (assets/series/). Environment plates done (assets/ep01/environments/). Storyboard complete: 28 panels reviewed and passed (assets/ep01/storyboard/README.md). Video: Seedance 2.5 one clip per event (one complex or two simple events, one camera setup, at most two lines), cut together in the edit; clip list in episodes/ep01/clip-list.md. The 30 s chunk drafts (assets/ep01/video/chunk0*) are superseded and kept for reference. Clips 01 to 40 (shots 1 to 19, cold open through Hopper setting up his transfer) rendered at 480p and passed, assembly assets/ep01/clips/ep01-clips01-40-assembled-480p.mp4 (about 3:45). Insert, POV and flat-graphic shots go still-first (docs/workflow.md). The four lesson talking-heads (clips 24, 26, 29, 31) were amended: rebuilt still-first as concept diagrams that fill the frame beside Kanga instead of her alone in empty space; clip 28 restaged (bag at side, not clutched); clip 32 redone so the guitar reads (old takes in clips/rejected/ with -v1). Prompt-optimizer skill installed at .claude/skills/prompt-optimizer/; Seedance eight-part director's-brief shape now in docs/workflow.md. Voice references: Kanga assets/series/kanga/kanga-voice-ref-opener.mp3, Hopper assets/series/hopper/hopper-voice-ref-ep01c3.mp3. Next: clips 41 to 50 (the turn and the payoff). Then 1080p re-renders of approved clips.
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
3. Follow the locked episode format above, and apply the screen time rule to every shot: cut or shorten any shot that neither makes the lesson clearer nor reveals character
4. Produce script.md first (26–30 shots, character bible header, production notes), then clip-list.md (one complex or two simple events per clip, see docs/workflow.md), then openart-prompts.md following the ep01 pattern: style string → characters → environments → storyboard list → Smart Shot sequences → image-to-video motion prompts → voice specs → assembly order → credit tips
